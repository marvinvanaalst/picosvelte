<script>
	import Sub from '$lib//text/Sub.svelte';
	import Button from '$lib/Button.svelte';
	import Card from '$lib/cards/card.svelte';
	import Link from '$lib/Link.svelte';
	import Nav from '$lib/nav/Nav.svelte';
	import NavItem from '$lib/nav/NavItem.svelte';
	import Rule from '$lib/Rule.svelte';
	import Footer from '$lib/sections/Footer.svelte';
	import Header from '$lib/sections/Header.svelte';
	import Main from '$lib/sections/Main.svelte';
	import Row from '$lib/sections/Row.svelte';
	import Section from '$lib/sections/Section.svelte';
	import Bold from '$lib/text/Bold.svelte';
	import H1 from '$lib/text/H1.svelte';
	import H2 from '$lib/text/H2.svelte';
	import H3 from '$lib/text/H3.svelte';
	import H4 from '$lib/text/H4.svelte';
	import H5 from '$lib/text/H5.svelte';
	import H6 from '$lib/text/H6.svelte';
	import Highlight from '$lib/text/Highlight.svelte';
	import Inserted from '$lib/text/Inserted.svelte';
	import Italic from '$lib/text/Italic.svelte';
	import Keyboard from '$lib/text/Keyboard.svelte';
	import Small from '$lib/text/Small.svelte';
	import Sup from '$lib/text/Sup.svelte';
	import Text from '$lib/text/Text.svelte';
	import Underline from '$lib/text/Underline.svelte';
</script>

<Nav>
	<NavItem href="/" name="Home" />
	<NavItem href="/" name="About" />
	<NavItem href="/" name="Blog" />
</Nav>
<Header>
	<H1 color="white">Glorious header</H1>
	<Text color="white">This could be a subtitle.</Text>
	<Text color="white">Or you could replace the whole thing with a hero image.</Text>
</Header>
<Main>
	<!-- Defaults -->
	<Section>
		<H1>Heading 1</H1>
		<H2>Heading 2</H2>
		<H3>Heading 3</H3>
		<H4>Heading 4</H4>
		<H5>Heading 5</H5>
		<H6>Heading 6</H6>
		<Text>
			Text looks like this, also maybe <Bold>bold</Bold> or with <Italic>emphasis</Italic>. Maybe it
			is <Small>small</Small> or <Sub>Low</Sub> or <Sup>High</Sup>, might be <Inserted
				>inserted</Inserted
			>, a <Highlight>highlight</Highlight>, some <Keyboard>keyboard entry</Keyboard> or <Underline
				>underlined</Underline
			>
		</Text>
		<Row>
			<Button>Button default</Button>
			<Button color="secondary">Button secondary</Button>
			<Button color="black">Button black</Button>
		</Row>
		<Row>
			<Text>Let's link to</Text>
			<Link href={'/'}>the primary color</Link>
			<Text>or</Text>
			<Link href={'/'} color="secondary">the secondary color</Link>
		</Row>
		<Row>
			<Card>
				<H1>Card heading</H1>
				<Text
					>Some text, it's important to fill the card so that it looks kinda good. Otherwise it can
					start to feel a bit empty, you know?
				</Text>
				<Link href="">Learn more</Link>
				<Rule />
			</Card>
			<Card>
				<H1>Card heading</H1>
				<Text
					>Some text, it's important to fill the card so that it looks kinda good. Otherwise it can
					start to feel a bit empty, you know?
				</Text>
				<Link href="">Learn more</Link>
				<Rule />
			</Card>
		</Row>
	</Section>
	<!-- Black section -->
	<Section color="black">
		<H1 color="white">Heading 1</H1>
		<H2 color="white">Heading 2</H2>
		<H3 color="white">Heading 3</H3>
		<H4 color="white">Heading 4</H4>
		<H5 color="white">Heading 5</H5>
		<H6 color="white">Heading 6</H6>
		<Text color="white">
			Text looks like this, also maybe <Bold>bold</Bold> or with <Italic>emphasis</Italic>. Maybe it
			is <Small>small</Small> or <Sub>Low</Sub> or <Sup>High</Sup>, might be <Inserted
				>inserted</Inserted
			>, a <Highlight>highlight</Highlight>, some <Keyboard>keyboard entry</Keyboard> or <Underline
				>underlined</Underline
			>
		</Text>
		<Row>
			<Button>Button default</Button>
			<Button color="secondary">Button secondary</Button>
			<Button color="white">Button white</Button>
		</Row>
		<Row>
			<Text color="white">Let's link using</Text>
			<Link href={'/'}>the primary color</Link>
			<Text color="white">or</Text>
			<Link href={'/'} color="secondary">the secondary color</Link>
		</Row>
	</Section>
	<!-- Primary -->
	<Section color="primary">
		<H1 color="white">Heading 1</H1>
		<H2 color="white">Heading 2</H2>
		<H3 color="white">Heading 3</H3>
		<H4 color="white">Heading 4</H4>
		<H5 color="white">Heading 5</H5>
		<H6 color="white">Heading 6</H6>
		<Text color="white">
			Text looks like this, also maybe <Bold>bold</Bold> or with <Italic>emphasis</Italic>. Maybe it
			is <Small>small</Small> or <Sub>Low</Sub> or <Sup>High</Sup>, might be <Inserted
				>inserted</Inserted
			>, a <Highlight>highlight</Highlight>, some <Keyboard>keyboard entry</Keyboard> or <Underline
				>underlined</Underline
			>
		</Text>
		<Row>
			<Button color="secondary">Button secondary</Button>
			<Button color="white">Button white</Button>
			<Button color="black">Button black</Button>
		</Row>
		<Row>
			<Text color="white">Let's link using</Text>
			<Link href={'/'} color="black">black</Link>
			<Text color="white">or</Text>
			<Link href={'/'} color="secondary">the secondary color</Link>
		</Row>
	</Section>
	<!-- Secondary -->
	<Section color="secondary">
		<H1>Heading 1</H1>
		<H2>Heading 2</H2>
		<H3>Heading 3</H3>
		<H4>Heading 4</H4>
		<H5>Heading 5</H5>
		<H6>Heading 6</H6>
		<Text>
			Text looks like this, also maybe <Bold>bold</Bold> or with <Italic>emphasis</Italic>. Maybe it
			is <Small>small</Small> or <Sub>Low</Sub> or <Sup>High</Sup>, might be <Inserted
				>inserted</Inserted
			>, a <Highlight>highlight</Highlight>, some <Keyboard>keyboard entry</Keyboard> or <Underline
				>underlined</Underline
			>
		</Text>
		<Row>
			<Button>Button default</Button>
			<Button color="white">Button white</Button>
			<Button color="black">Button black</Button>
		</Row>
		<Row>
			<Text>Let's link using</Text>
			<Link href={'/'}>the primary color</Link>
			<Text>or</Text>
			<Link href={'/'} color="white">white</Link>
		</Row>
	</Section>
</Main>
<Footer>
	<H2 color="white">Footer</H2>
	<Text color="white">Here is loads of space to write about the boring stuff.</Text>
	<Text color="white">Like legal information.</Text>
</Footer>
