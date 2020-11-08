---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2261AD64-196A-402E-9703-EFB3A6D75FA7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83ed3e336ca72e38fc16c27ec696eea0f84f746
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029680"
---
# <span data-ttu-id="f2bb2-101">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="f2bb2-101">New-AzureServiceProject</span></span>

## <span data-ttu-id="f2bb2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="f2bb2-103">Crea i file e la configurazione necessari per un nuovo servizio.</span><span class="sxs-lookup"><span data-stu-id="f2bb2-103">Creates the required files and configuration for a new service.</span></span>

## <span data-ttu-id="f2bb2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2bb2-104">SYNTAX</span></span>

```
New-AzureServiceProject -ServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f2bb2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2bb2-105">DESCRIPTION</span></span>
<span data-ttu-id="f2bb2-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f2bb2-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f2bb2-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f2bb2-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f2bb2-108">Il cmdlet **New-AzureServiceProject** crea i file e la configurazione necessari per un nuovo servizio Azure nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="f2bb2-108">The **New-AzureServiceProject** cmdlet creates the required files and configuration for a new Azure service in the current directory.</span></span>

## <span data-ttu-id="f2bb2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2bb2-109">EXAMPLES</span></span>

### <span data-ttu-id="f2bb2-110">Esempio 1: creare ponteggi per un servizio</span><span class="sxs-lookup"><span data-stu-id="f2bb2-110">Example 1: Create scaffolding for a service</span></span>
```
PS C:\> New-AzureServiceProject MyService1
```

<span data-ttu-id="f2bb2-111">Questo esempio crea ponteggi per un nuovo servizio Azure denominato MyService1 nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="f2bb2-111">This example creates scaffolding for a new Azure service named MyService1 in the current directory.</span></span>

## <span data-ttu-id="f2bb2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2bb2-112">PARAMETERS</span></span>

### <span data-ttu-id="f2bb2-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="f2bb2-113">-Profile</span></span>
<span data-ttu-id="f2bb2-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2bb2-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f2bb2-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="f2bb2-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f2bb2-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f2bb2-116">-ServiceName</span></span>
<span data-ttu-id="f2bb2-117">Specifica il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="f2bb2-117">Specifies the name of the service.</span></span>
<span data-ttu-id="f2bb2-118">Determina la prima sezione del nome host per il servizio (ad esempio, name.cloudapp.net) e la directory che conterrà il servizio.</span><span class="sxs-lookup"><span data-stu-id="f2bb2-118">It determines the first section of the hostname for your service (for example, name.cloudapp.net), and the directory that will contain your service.</span></span>
<span data-ttu-id="f2bb2-119">Il nome può contenere solo lettere, cifre e il carattere di trattino (-).</span><span class="sxs-lookup"><span data-stu-id="f2bb2-119">The name can contain only letters, digits, and the dash character (-).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2bb2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2bb2-120">CommonParameters</span></span>
<span data-ttu-id="f2bb2-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2bb2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2bb2-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2bb2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2bb2-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2bb2-123">INPUTS</span></span>

## <span data-ttu-id="f2bb2-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2bb2-124">OUTPUTS</span></span>

## <span data-ttu-id="f2bb2-125">Note</span><span class="sxs-lookup"><span data-stu-id="f2bb2-125">NOTES</span></span>

## <span data-ttu-id="f2bb2-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2bb2-126">RELATED LINKS</span></span>

[<span data-ttu-id="f2bb2-127">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="f2bb2-127">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="f2bb2-128">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="f2bb2-128">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="f2bb2-129">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="f2bb2-129">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="f2bb2-130">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="f2bb2-130">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)

[<span data-ttu-id="f2bb2-131">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="f2bb2-131">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)


