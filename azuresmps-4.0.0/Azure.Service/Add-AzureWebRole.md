---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FB5CD696-108D-4A3E-8983-1C6562E8795A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25ade8ccf395d37ab0856742fe473a6508c9d63b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023669"
---
# <span data-ttu-id="c817d-101">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="c817d-101">Add-AzureWebRole</span></span>

## <span data-ttu-id="c817d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c817d-102">SYNOPSIS</span></span>
<span data-ttu-id="c817d-103">Aggiunge un ruolo di lavoro Web.</span><span class="sxs-lookup"><span data-stu-id="c817d-103">Adds a web worker role.</span></span>

## <span data-ttu-id="c817d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c817d-104">SYNTAX</span></span>

```
Add-AzureWebRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c817d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c817d-105">DESCRIPTION</span></span>
<span data-ttu-id="c817d-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c817d-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c817d-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c817d-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c817d-108">Il cmdlet **Add-AzureWebRole** aggiunge un ruolo di lavoro Web.</span><span class="sxs-lookup"><span data-stu-id="c817d-108">The **Add-AzureWebRole** cmdlet adds a web worker role.</span></span>

## <span data-ttu-id="c817d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c817d-109">EXAMPLES</span></span>

### <span data-ttu-id="c817d-110">Esempio 1: aggiungere un ruolo predefinito</span><span class="sxs-lookup"><span data-stu-id="c817d-110">Example 1: Add a default role</span></span>
```
PS C:\> Add-AzureWebRole
```

<span data-ttu-id="c817d-111">Questo comando aggiunge il ruolo Web con la configurazione predefinita di Webrole1 come nome e una singola istanza.</span><span class="sxs-lookup"><span data-stu-id="c817d-111">This command add web role that has the default configuration of Webrole1 as the name and a single instance.</span></span>

### <span data-ttu-id="c817d-112">Esempio 2: aggiungere un ruolo con un nome</span><span class="sxs-lookup"><span data-stu-id="c817d-112">Example 2: Add a role with a name</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole"
```

<span data-ttu-id="c817d-113">Questo comando aggiunge un singolo ruolo Web denominato MyWebRole all'applicazione corrente.</span><span class="sxs-lookup"><span data-stu-id="c817d-113">This command adds a single web role named MyWebRole to the current application.</span></span>

### <span data-ttu-id="c817d-114">Esempio 3: aggiungere un ruolo con un nome e un conteggio delle istanze</span><span class="sxs-lookup"><span data-stu-id="c817d-114">Example 3: Add a role with a name and instance count</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -Instance 2
```

<span data-ttu-id="c817d-115">Questo comando aggiunge un ruolo Web denominato MyWebRole all'applicazione corrente.</span><span class="sxs-lookup"><span data-stu-id="c817d-115">This command adds a web role named MyWebRole to the current application.</span></span>
<span data-ttu-id="c817d-116">Il cmdlet ha un conteggio delle istanze del ruolo di 2.</span><span class="sxs-lookup"><span data-stu-id="c817d-116">The cmdlet has a role instance count of 2.</span></span>

### <span data-ttu-id="c817d-117">Esempio 4: aggiungere un ruolo con un nome e un modello</span><span class="sxs-lookup"><span data-stu-id="c817d-117">Example 4: Add a role with a name and template</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -TemplateFolder ".\MyWebTemplateFolder"
```

<span data-ttu-id="c817d-118">Questo comando aggiunge un singolo ruolo Web denominato MyWebRole all'applicazione corrente.</span><span class="sxs-lookup"><span data-stu-id="c817d-118">This command adds a single web role named MyWebRole to the current application.</span></span>
<span data-ttu-id="c817d-119">Il comando specifica una cartella denominata MyWebTemplateFolder come modello di ponteggi.</span><span class="sxs-lookup"><span data-stu-id="c817d-119">The command specifies a folder named MyWebTemplateFolder as a scaffolding template.</span></span>

## <span data-ttu-id="c817d-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c817d-120">PARAMETERS</span></span>

### <span data-ttu-id="c817d-121">-Istanze</span><span class="sxs-lookup"><span data-stu-id="c817d-121">-Instances</span></span>
<span data-ttu-id="c817d-122">Specifica il numero di istanze.</span><span class="sxs-lookup"><span data-stu-id="c817d-122">Specifies the number of instances.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c817d-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="c817d-123">-Name</span></span>
<span data-ttu-id="c817d-124">Specifica il nome del ruolo Web.</span><span class="sxs-lookup"><span data-stu-id="c817d-124">Specifies the name of the web role.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c817d-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="c817d-125">-Profile</span></span>
<span data-ttu-id="c817d-126">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c817d-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c817d-127">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c817d-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c817d-128">-TemplateFolder</span><span class="sxs-lookup"><span data-stu-id="c817d-128">-TemplateFolder</span></span>
<span data-ttu-id="c817d-129">Specifica la cartella modello.</span><span class="sxs-lookup"><span data-stu-id="c817d-129">Specifies the template folder.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c817d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c817d-130">CommonParameters</span></span>
<span data-ttu-id="c817d-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c817d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c817d-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c817d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c817d-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c817d-133">INPUTS</span></span>

## <span data-ttu-id="c817d-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c817d-134">OUTPUTS</span></span>

## <span data-ttu-id="c817d-135">Note</span><span class="sxs-lookup"><span data-stu-id="c817d-135">NOTES</span></span>

## <span data-ttu-id="c817d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c817d-136">RELATED LINKS</span></span>

[<span data-ttu-id="c817d-137">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="c817d-137">Add-AzureWorkerRole</span></span>](./Add-AzureWorkerRole.md)

[<span data-ttu-id="c817d-138">New-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="c817d-138">New-AzureRoleTemplate</span></span>](./New-AzureRoleTemplate.md)


