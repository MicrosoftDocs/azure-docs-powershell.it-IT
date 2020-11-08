---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 756F757C-8CDE-43A5-A8A6-D55EF9C66183
online version: ''
schema: 2.0.0
ms.openlocfilehash: 71402e56251e2632c73a9185a1e70b4e3de8d770
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023959"
---
# <span data-ttu-id="fdd20-101">New-AzureMediaServicesKey</span><span class="sxs-lookup"><span data-stu-id="fdd20-101">New-AzureMediaServicesKey</span></span>

## <span data-ttu-id="fdd20-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fdd20-102">SYNOPSIS</span></span>
<span data-ttu-id="fdd20-103">Aggiorna le chiavi degli account di Azure Media Services.</span><span class="sxs-lookup"><span data-stu-id="fdd20-103">Updates Azure Media Services account keys.</span></span>

<span data-ttu-id="fdd20-104">**Nota:** Questa versione è deprecata, vedere la [versione più recente](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="fdd20-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="fdd20-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fdd20-105">SYNTAX</span></span>

```
New-AzureMediaServicesKey -Name <String> -KeyType <MediaServicesKeyType> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdd20-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdd20-106">DESCRIPTION</span></span>
<span data-ttu-id="fdd20-107">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fdd20-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="fdd20-108">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="fdd20-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="fdd20-109">Il cmdlet **New-AzureMediaServicesKey** aggiorna la chiave primaria o secondaria per l'account di servizi multimediali specificato.</span><span class="sxs-lookup"><span data-stu-id="fdd20-109">The **New-AzureMediaServicesKey** cmdlet updates the Primary or Secondary key for the specified Media Services account.</span></span>

## <span data-ttu-id="fdd20-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fdd20-110">EXAMPLES</span></span>

### <span data-ttu-id="fdd20-111">Esempio 1: aggiornare una chiave dell'account di servizi multimediali</span><span class="sxs-lookup"><span data-stu-id="fdd20-111">Example 1: Update a Media Services account key</span></span>
```
PS C:\> New-AzureMediaServicesKey -Name "mediaservicesaccount" -KeyType "Primary" -Force
```

## <span data-ttu-id="fdd20-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fdd20-112">PARAMETERS</span></span>

### <span data-ttu-id="fdd20-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fdd20-113">-Force</span></span>
<span data-ttu-id="fdd20-114">Indica che la generazione della chiave non è confermata.</span><span class="sxs-lookup"><span data-stu-id="fdd20-114">Indicates that the key generation is not confirmed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdd20-115">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="fdd20-115">-KeyType</span></span>
<span data-ttu-id="fdd20-116">Specifica il tipo di chiave servizi multimediali; I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="fdd20-116">Specifies the Media Services key type; Valid values are:</span></span>
  
- <span data-ttu-id="fdd20-117">Principale</span><span class="sxs-lookup"><span data-stu-id="fdd20-117">Primary</span></span>
- <span data-ttu-id="fdd20-118">Secondario</span><span class="sxs-lookup"><span data-stu-id="fdd20-118">Secondary</span></span>

```yaml
Type: MediaServicesKeyType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdd20-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="fdd20-119">-Name</span></span>
<span data-ttu-id="fdd20-120">Specifica il nome dell'account di servizi multimediali.</span><span class="sxs-lookup"><span data-stu-id="fdd20-120">Specifies the name of the Media Services account.</span></span>

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

### <span data-ttu-id="fdd20-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="fdd20-121">-Profile</span></span>
<span data-ttu-id="fdd20-122">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdd20-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fdd20-123">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="fdd20-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fdd20-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fdd20-124">-Confirm</span></span>
<span data-ttu-id="fdd20-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdd20-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdd20-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdd20-126">-WhatIf</span></span>
<span data-ttu-id="fdd20-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdd20-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdd20-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdd20-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdd20-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdd20-129">CommonParameters</span></span>
<span data-ttu-id="fdd20-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdd20-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdd20-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdd20-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdd20-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fdd20-132">INPUTS</span></span>

## <span data-ttu-id="fdd20-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fdd20-133">OUTPUTS</span></span>

## <span data-ttu-id="fdd20-134">Note</span><span class="sxs-lookup"><span data-stu-id="fdd20-134">NOTES</span></span>

## <span data-ttu-id="fdd20-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fdd20-135">RELATED LINKS</span></span>

[<span data-ttu-id="fdd20-136">Come usare Azure PowerShell per i servizi multimediali</span><span class="sxs-lookup"><span data-stu-id="fdd20-136">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)


