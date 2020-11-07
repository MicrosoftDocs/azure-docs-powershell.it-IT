---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: ccb40de9ef5e9e68cf62b7b05edeaac9ae10efbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674674"
---
# <span data-ttu-id="aebe1-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="aebe1-101">New-AzDataShare</span></span>

## <span data-ttu-id="aebe1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aebe1-102">SYNOPSIS</span></span>
<span data-ttu-id="aebe1-103">Crea una condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="aebe1-103">Creates a azure data share.</span></span>

## <span data-ttu-id="aebe1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aebe1-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aebe1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aebe1-105">DESCRIPTION</span></span>
<span data-ttu-id="aebe1-106">Il cmdlet **New-AzDataShare** crea una condivisione dati all'interno di un account di condivisione dati di Azure specificato fornendo il nome del gruppo di risorse, il nome dell'account, il nome della condivisione e il tipo di condivisione.</span><span class="sxs-lookup"><span data-stu-id="aebe1-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="aebe1-107">Descrizione e condizioni per l'uso sono parametri facoltativi che possono essere impostati durante la creazione della condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="aebe1-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="aebe1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aebe1-108">EXAMPLES</span></span>

### <span data-ttu-id="aebe1-109">Esempio 1: creare una condivisione dati</span><span class="sxs-lookup"><span data-stu-id="aebe1-109">Example 1 : Create a data share</span></span>
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

<span data-ttu-id="aebe1-110">Questo comando crea una condivisione dati denominata AdsShare di tipo CopyBased nell'account di condivisione dati WikiAdsAccount in annunci gruppo risorse con descrizione e condizioni per l'uso.</span><span class="sxs-lookup"><span data-stu-id="aebe1-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="aebe1-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aebe1-111">PARAMETERS</span></span>

### <span data-ttu-id="aebe1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="aebe1-112">-AccountName</span></span>
<span data-ttu-id="aebe1-113">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="aebe1-113">Azure data share account name</span></span>

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

### <span data-ttu-id="aebe1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aebe1-114">-DefaultProfile</span></span>
<span data-ttu-id="aebe1-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aebe1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aebe1-116">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="aebe1-116">-Description</span></span>
<span data-ttu-id="aebe1-117">Descrizione della condivisione di dati di Azure</span><span class="sxs-lookup"><span data-stu-id="aebe1-117">Description of azure data share</span></span>

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

### <span data-ttu-id="aebe1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="aebe1-118">-Name</span></span>
<span data-ttu-id="aebe1-119">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="aebe1-119">Azure data share name</span></span>

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

### <span data-ttu-id="aebe1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aebe1-120">-ResourceGroupName</span></span>
<span data-ttu-id="aebe1-121">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="aebe1-121">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="aebe1-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="aebe1-122">-TermsOfUse</span></span>
<span data-ttu-id="aebe1-123">Condizioni per l'uso della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="aebe1-123">Terms of use for azure data share</span></span>

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

### <span data-ttu-id="aebe1-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aebe1-124">-Confirm</span></span>
<span data-ttu-id="aebe1-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aebe1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aebe1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aebe1-126">-WhatIf</span></span>
<span data-ttu-id="aebe1-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aebe1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aebe1-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aebe1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aebe1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aebe1-129">CommonParameters</span></span>
<span data-ttu-id="aebe1-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aebe1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aebe1-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aebe1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aebe1-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aebe1-132">INPUTS</span></span>

### <span data-ttu-id="aebe1-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="aebe1-133">None</span></span>

## <span data-ttu-id="aebe1-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aebe1-134">OUTPUTS</span></span>

### <span data-ttu-id="aebe1-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="aebe1-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="aebe1-136">Note</span><span class="sxs-lookup"><span data-stu-id="aebe1-136">NOTES</span></span>

## <span data-ttu-id="aebe1-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aebe1-137">RELATED LINKS</span></span>
