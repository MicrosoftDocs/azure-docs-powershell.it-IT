---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E499868E-A745-4CA4-A717-C33C3B94A2C8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b80071bb82ebbb960be5b5b4fcc854dc47c9ed9d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023950"
---
# <span data-ttu-id="92bd6-101">New-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="92bd6-101">New-AzureRoleTemplate</span></span>

## <span data-ttu-id="92bd6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="92bd6-102">SYNOPSIS</span></span>
<span data-ttu-id="92bd6-103">Crea modelli di ruolo Web e lavoro.</span><span class="sxs-lookup"><span data-stu-id="92bd6-103">Creates web and worker role templates.</span></span>

## <span data-ttu-id="92bd6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92bd6-104">SYNTAX</span></span>

### <span data-ttu-id="92bd6-105">WebRole</span><span class="sxs-lookup"><span data-stu-id="92bd6-105">WebRole</span></span>
```
New-AzureRoleTemplate [-Web] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="92bd6-106">WorkerRole</span><span class="sxs-lookup"><span data-stu-id="92bd6-106">WorkerRole</span></span>
```
New-AzureRoleTemplate [-Worker] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="92bd6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92bd6-107">DESCRIPTION</span></span>
<span data-ttu-id="92bd6-108">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="92bd6-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="92bd6-109">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="92bd6-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="92bd6-110">Il cmdlet **New-AzureRoleTemplate** crea modelli di ruoli Web e worker.</span><span class="sxs-lookup"><span data-stu-id="92bd6-110">The **New-AzureRoleTemplate** cmdlet creates web and worker role templates.</span></span>

## <span data-ttu-id="92bd6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92bd6-111">EXAMPLES</span></span>

### <span data-ttu-id="92bd6-112">Esempio 1: creare un modello di ruolo Web</span><span class="sxs-lookup"><span data-stu-id="92bd6-112">Example 1: Create a web role template</span></span>
```
PS C:\> New-AzureRoleTemplate -Web
```

<span data-ttu-id="92bd6-113">Questo esempio crea un nuovo modello di ruolo Web in una cartella denominata WebRoleTemplate nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="92bd6-113">This example creates a new web role template in a folder named WebRoleTemplate in the current directory.</span></span>

### <span data-ttu-id="92bd6-114">Esempio 2: creare un modello di ruolo di lavoro</span><span class="sxs-lookup"><span data-stu-id="92bd6-114">Example 2: Create a worker role template</span></span>
```
PS C:\> New-AzureRoleTemplate -Worker
```

<span data-ttu-id="92bd6-115">Questo esempio crea un nuovo modello di ruolo di lavoro in una cartella denominata WebRoleTemplate nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="92bd6-115">This example creates a new worker role template in a folder named WebRoleTemplate in the current directory.</span></span>

### <span data-ttu-id="92bd6-116">Esempio 3: creare un modello di ruolo in una directory personalizzata</span><span class="sxs-lookup"><span data-stu-id="92bd6-116">Example 3: Create a role template in a custom directory</span></span>
```
PS C:\> New-AzureRoleTemplate -Web -Output C:\MyWebRoleTemplate
```

<span data-ttu-id="92bd6-117">Questo esempio crea un nuovo modello di ruolo Web nella directory denominata MyWebRoleTemplate, anziché nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="92bd6-117">This example creates a new web role template in directory named MyWebRoleTemplate, instead of in the current directory.</span></span>

## <span data-ttu-id="92bd6-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="92bd6-118">PARAMETERS</span></span>

### <span data-ttu-id="92bd6-119">-Output</span><span class="sxs-lookup"><span data-stu-id="92bd6-119">-Output</span></span>
<span data-ttu-id="92bd6-120">Specifica il percorso di output del modello generato.</span><span class="sxs-lookup"><span data-stu-id="92bd6-120">Specifies the output path of generated template.</span></span>

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

### <span data-ttu-id="92bd6-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="92bd6-121">-Profile</span></span>
<span data-ttu-id="92bd6-122">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92bd6-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="92bd6-123">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="92bd6-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="92bd6-124">-Web</span><span class="sxs-lookup"><span data-stu-id="92bd6-124">-Web</span></span>
<span data-ttu-id="92bd6-125">Specifica che si vuole creare un modello di ruolo Web.</span><span class="sxs-lookup"><span data-stu-id="92bd6-125">Specifies that you want to create a web role template.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92bd6-126">-Lavoratore</span><span class="sxs-lookup"><span data-stu-id="92bd6-126">-Worker</span></span>
<span data-ttu-id="92bd6-127">Specifica che si vuole creare un modello di ruolo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="92bd6-127">Specifies that you want to create a worker role template.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WorkerRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92bd6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92bd6-128">CommonParameters</span></span>
<span data-ttu-id="92bd6-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92bd6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92bd6-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92bd6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92bd6-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="92bd6-131">INPUTS</span></span>

## <span data-ttu-id="92bd6-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92bd6-132">OUTPUTS</span></span>

## <span data-ttu-id="92bd6-133">Note</span><span class="sxs-lookup"><span data-stu-id="92bd6-133">NOTES</span></span>

## <span data-ttu-id="92bd6-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92bd6-134">RELATED LINKS</span></span>

[<span data-ttu-id="92bd6-135">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="92bd6-135">Add-AzureWebRole</span></span>](./Add-AzureWebRole.md)

[<span data-ttu-id="92bd6-136">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="92bd6-136">Add-AzureWorkerRole</span></span>](./Add-AzureWorkerRole.md)


