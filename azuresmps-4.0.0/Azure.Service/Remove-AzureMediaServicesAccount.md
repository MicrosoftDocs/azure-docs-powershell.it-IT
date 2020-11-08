---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5B255D11-0A9B-4679-A2AC-4357B293EE96
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4eee130312ae52e95b020151750d46144bc3685
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029933"
---
# <span data-ttu-id="53596-101">Remove-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="53596-101">Remove-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="53596-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53596-102">SYNOPSIS</span></span>
<span data-ttu-id="53596-103">Rimuove l'account di servizi di Azure Media specificato.</span><span class="sxs-lookup"><span data-stu-id="53596-103">Removes the specified Azure Media Services account.</span></span>

<span data-ttu-id="53596-104">**Nota:**  Questa versione è deprecata, vedere la [versione più recente](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="53596-104">**Note:**  This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="53596-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53596-105">SYNTAX</span></span>

```
Remove-AzureMediaServicesAccount -Name <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53596-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53596-106">DESCRIPTION</span></span>
<span data-ttu-id="53596-107">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="53596-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="53596-108">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="53596-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="53596-109">Il cmdlet **Remove-AzureMediaServicesAccount** rimuove un account di servizi multimediali.</span><span class="sxs-lookup"><span data-stu-id="53596-109">The **Remove-AzureMediaServicesAccount** cmdlet removes a Media Services account.</span></span>

## <span data-ttu-id="53596-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53596-110">EXAMPLES</span></span>

### <span data-ttu-id="53596-111">Esempio 1: eliminare un account di servizi multimediali</span><span class="sxs-lookup"><span data-stu-id="53596-111">Example 1: Delete a Media Services account</span></span>
```
PS C:\> Remove-AzureMediaServicesAccount -Name "mediaservicesaccount" -Force
```

## <span data-ttu-id="53596-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53596-112">PARAMETERS</span></span>

### <span data-ttu-id="53596-113">-Force</span><span class="sxs-lookup"><span data-stu-id="53596-113">-Force</span></span>
<span data-ttu-id="53596-114">Se viene specificato l'opzione *Force* , l'eliminazione non viene confermata.</span><span class="sxs-lookup"><span data-stu-id="53596-114">If the *Force* switch is specified, the deletion is not confirmed.</span></span>

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

### <span data-ttu-id="53596-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="53596-115">-Name</span></span>
<span data-ttu-id="53596-116">Nome dell'account dei servizi multimediali.</span><span class="sxs-lookup"><span data-stu-id="53596-116">The Media Services account name.</span></span>

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

### <span data-ttu-id="53596-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="53596-117">-Profile</span></span>
<span data-ttu-id="53596-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53596-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="53596-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="53596-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="53596-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="53596-120">-Confirm</span></span>
<span data-ttu-id="53596-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53596-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53596-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53596-122">-WhatIf</span></span>
<span data-ttu-id="53596-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53596-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53596-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53596-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53596-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53596-125">CommonParameters</span></span>
<span data-ttu-id="53596-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53596-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53596-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53596-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53596-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53596-128">INPUTS</span></span>

## <span data-ttu-id="53596-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53596-129">OUTPUTS</span></span>

## <span data-ttu-id="53596-130">Note</span><span class="sxs-lookup"><span data-stu-id="53596-130">NOTES</span></span>

## <span data-ttu-id="53596-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53596-131">RELATED LINKS</span></span>

[<span data-ttu-id="53596-132">Come usare Azure PowerShell per i servizi multimediali</span><span class="sxs-lookup"><span data-stu-id="53596-132">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)

[<span data-ttu-id="53596-133">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="53596-133">Get-AzureMediaServicesAccount</span></span>](./Get-AzureMediaServicesAccount.md)

[<span data-ttu-id="53596-134">New-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="53596-134">New-AzureMediaServicesAccount</span></span>](./New-AzureMediaServicesAccount.md)


