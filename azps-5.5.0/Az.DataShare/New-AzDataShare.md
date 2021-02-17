---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: 265f917068237fee13f77eb8c87e0adf8cd12f08
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186103"
---
# <span data-ttu-id="e3858-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="e3858-101">New-AzDataShare</span></span>

## <span data-ttu-id="e3858-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3858-102">SYNOPSIS</span></span>
<span data-ttu-id="e3858-103">Crea una condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="e3858-103">Creates a azure data share.</span></span>

## <span data-ttu-id="e3858-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3858-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3858-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e3858-105">DESCRIPTION</span></span>
<span data-ttu-id="e3858-106">Il cmdlet **New-AzDataShare** crea una condivisione dati all'interno di un account di condivisione dati azure specificato fornendo il nome del gruppo di risorse, il nome dell'account, il nome della condivisione e il tipo di condivisione.</span><span class="sxs-lookup"><span data-stu-id="e3858-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="e3858-107">La descrizione e i termini di utilizzo sono parametri facoltativi che è possibile impostare durante la creazione della condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="e3858-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="e3858-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3858-108">EXAMPLES</span></span>

### <span data-ttu-id="e3858-109">Esempio 1: Creare una condivisione dati</span><span class="sxs-lookup"><span data-stu-id="e3858-109">Example 1 : Create a data share</span></span>
```
PS C:\>New-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -ShareKind "CopyBased" -Description "Example of description" -TermsOfUse "This should not be shared"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="e3858-110">Questo comando crea una condivisione dati denominata AdsShare del tipo CopyBased nell'account di condivisione dati WikiAdsAccount nel gruppo di risorse ADS con una descrizione e le condizioni per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="e3858-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="e3858-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3858-111">PARAMETERS</span></span>

### <span data-ttu-id="e3858-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e3858-112">-AccountName</span></span>
<span data-ttu-id="e3858-113">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="e3858-113">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3858-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3858-114">-DefaultProfile</span></span>
<span data-ttu-id="e3858-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3858-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3858-116">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3858-116">-Description</span></span>
<span data-ttu-id="e3858-117">Descrizione della condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="e3858-117">Description of azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3858-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e3858-118">-Name</span></span>
<span data-ttu-id="e3858-119">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="e3858-119">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3858-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3858-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3858-121">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="e3858-121">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3858-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="e3858-122">-TermsOfUse</span></span>
<span data-ttu-id="e3858-123">Condizioni per l'utilizzo per la condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="e3858-123">Terms of use for azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3858-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3858-124">-Confirm</span></span>
<span data-ttu-id="e3858-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3858-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3858-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3858-126">-WhatIf</span></span>
<span data-ttu-id="e3858-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3858-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3858-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3858-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3858-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3858-129">CommonParameters</span></span>
<span data-ttu-id="e3858-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3858-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3858-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e3858-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3858-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="e3858-132">INPUTS</span></span>

### <span data-ttu-id="e3858-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e3858-133">None</span></span>

## <span data-ttu-id="e3858-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3858-134">OUTPUTS</span></span>

### <span data-ttu-id="e3858-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="e3858-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="e3858-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="e3858-136">NOTES</span></span>

## <span data-ttu-id="e3858-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3858-137">RELATED LINKS</span></span>
