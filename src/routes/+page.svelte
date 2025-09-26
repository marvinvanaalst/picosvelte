<script>
	import Sub from '$lib/pico//text/Sub.svelte';
	import Btn3Grid from '$lib/pico/buttons/Btn3Grid.svelte';
	import Button from '$lib/pico/buttons/PrimaryButton.svelte';
	import SecondaryButton from '$lib/pico/buttons/SecondaryButton.svelte';
	import Card from '$lib/pico/cards/Card.svelte';
	import CardRow from '$lib/pico/cards/CardRow.svelte';
	import Link from '$lib/pico/Link.svelte';

	import Rule from '$lib/pico/Rule.svelte';
	import Footer from '$lib/pico/sections/Footer.svelte';
	import Header from '$lib/pico/sections/Header.svelte';
	import Main from '$lib/pico/sections/Main.svelte';
	import Row from '$lib/pico/sections/Row.svelte';
	import Section from '$lib/pico/sections/Section.svelte';
	import Bold from '$lib/pico/text/Bold.svelte';
	import H1 from '$lib/pico/text/H1.svelte';
	import H2 from '$lib/pico/text/H2.svelte';
	import Highlight from '$lib/pico/text/Highlight.svelte';
	import Inserted from '$lib/pico/text/Inserted.svelte';
	import Italic from '$lib/pico/text/Italic.svelte';
	import Keyboard from '$lib/pico/text/Keyboard.svelte';
	import Small from '$lib/pico/text/Small.svelte';
	import Sup from '$lib/pico/text/Sup.svelte';
	import Text from '$lib/pico/text/Text.svelte';
	import Underline from '$lib/pico/text/Underline.svelte';
</script>

<Header>
	<H1 color="contrast" lineHeight="tight">Glorious header</H1>
	<Text color="contrast"
		>This could be a subtitle. Or you could replace the whole thing with a hero image?
	</Text>
</Header>
<Main>
	<!-- Defaults -->
	<Section>
		<H2>Default section</H2>
		<Text>
			Text looks like this, also maybe <Bold>bold</Bold> or with <Italic>emphasis</Italic>. Maybe it
			is <Small>small</Small> or <Sub>Low</Sub> or <Sup>High</Sup>, might be <Inserted
				>inserted</Inserted
			>, a <Highlight>highlight</Highlight>, some <Keyboard>keyboard entry</Keyboard> or <Underline
				>underlined</Underline
			>
		</Text>
		<Btn3Grid>
			<Button>Default</Button>
			<Button color="secondary">Secondary</Button>
			<Button color="dark">Dark</Button>
		</Btn3Grid>
		<Btn3Grid>
			<SecondaryButton>Default</SecondaryButton>
			<SecondaryButton color="secondary">Secondary</SecondaryButton>
			<SecondaryButton color="dark">Dark</SecondaryButton>
		</Btn3Grid>
		<Row>
			<Text>Let's link to <Link href={'/'}>the primary color</Link> something.</Text>
		</Row>
		<CardRow>
			<Card>
				<H2>Card heading</H2>
				<Text
					>Some text, it's important to fill the card so that it looks kinda good. Otherwise it can
					start to feel a bit empty, you know?
				</Text>
				<Link href="">Learn more</Link>
				<Rule />
			</Card>
			<Card>
				<H2>Card heading</H2>
				<Text
					>Some text, it's important to fill the card so that it looks kinda good. Otherwise it can
					start to feel a bit empty, you know?
				</Text>
				<Link href="">Learn more</Link>
				<Rule />
			</Card>
		</CardRow>
	</Section>

	<!-- Primary -->
	<Section color="primary">
		<H1 color="contrast">Primary section</H1>
		<H2 color="contrast">Heading 2</H2>
		<Text color="contrast">
			Text looks like this, also maybe <Bold>bold</Bold> or with <Italic>emphasis</Italic>. Maybe it
			is <Small>small</Small> or <Sub>Low</Sub> or <Sup>High</Sup>, might be <Inserted
				>inserted</Inserted
			>, a <Highlight>highlight</Highlight>, some <Keyboard>keyboard entry</Keyboard> or <Underline
				>underlined</Underline
			>
		</Text>
		<Btn3Grid>
			<Button color="secondary">Button secondary</Button>
			<Button color="white">Button white</Button>
			<Button color="black">Button black</Button>
		</Btn3Grid>
		<Row>
			<Text color="white"
				>Let's link to <Link href={'/'} color="white">the primary color</Link> something.</Text
			>
		</Row>
	</Section>
	<!-- Secondary -->
	<Section color="secondary">
		<H1 color="contrast">Secondary section</H1>
		<H2 color="contrast">Heading 2</H2>
		<Text color="contrast">
			Text looks like this, also maybe <Bold>bold</Bold> or with <Italic>emphasis</Italic>. Maybe it
			is <Small>small</Small> or <Sub>Low</Sub> or <Sup>High</Sup>, might be <Inserted
				>inserted</Inserted
			>, a <Highlight>highlight</Highlight>, some <Keyboard>keyboard entry</Keyboard> or <Underline
				>underlined</Underline
			>
		</Text>
		<Btn3Grid>
			<Button>Button default</Button>
			<Button color="white">Button white</Button>
			<Button color="black">Button black</Button>
		</Btn3Grid>
		<Row>
			<Text color="white"
				>Let's link to <Link href={'/'} color="white">the primary color</Link> something.</Text
			>
		</Row>
	</Section>
</Main>
<Footer>
	<H2 color="contrast">Footer</H2>
	<Text color="contrast">Here is loads of space to write about the boring stuff.</Text>
	<Text color="contrast">Like legal information.</Text>
</Footer>
