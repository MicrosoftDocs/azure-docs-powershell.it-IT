---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: 265f917068237fee13f77eb8c87e0adf8cd12f08
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297469"
---
# <span data-ttu-id="600d8-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="600d8-101">New-AzDataShare</span></span>

## <span data-ttu-id="600d8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="600d8-102">SYNOPSIS</span></span>
<span data-ttu-id="600d8-103">Crea una condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="600d8-103">Creates a azure data share.</span></span>

## <span data-ttu-id="600d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="600d8-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="600d8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="600d8-105">DESCRIPTION</span></span>
<span data-ttu-id="600d8-106">Il cmdlet **New-AzDataShare** crea una condivisione dati all'interno di un account di condivisione dati di Azure specificato fornendo il nome del gruppo di risorse, il nome dell'account, il nome della condivisione e il tipo di condivisione.</span><span class="sxs-lookup"><span data-stu-id="600d8-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="600d8-107">Descrizione e condizioni per l'uso sono parametri facoltativi che possono essere impostati durante la creazione della condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="600d8-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="600d8-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="600d8-108">EXAMPLES</span></span>

### <span data-ttu-id="600d8-109">Esempio 1: creare una condivisione dati</span><span class="sxs-lookup"><span data-stu-id="600d8-109">Example 1 : Create a data share</span></span>
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

<span data-ttu-id="600d8-110">Questo comando crea una condivisione dati denominata AdsShare di tipo CopyBased nell'account di condivisione dati WikiAdsAccount in annunci gruppo risorse con descrizione e condizioni per l'uso.</span><span class="sxs-lookup"><span data-stu-id="600d8-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="600d8-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="600d8-111">PARAMETERS</span></span>

### <span data-ttu-id="600d8-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="600d8-112">-AccountName</span></span>
<span data-ttu-id="600d8-113">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="600d8-113">Azure data share account name</span></span>

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

### <span data-ttu-id="600d8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="600d8-114">-DefaultProfile</span></span>
<span data-ttu-id="600d8-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="600d8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="600d8-116">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="600d8-116">-Description</span></span>
<span data-ttu-id="600d8-117">Descrizione della condivisione di dati di Azure</span><span class="sxs-lookup"><span data-stu-id="600d8-117">Description of azure data share</span></span>

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

### <span data-ttu-id="600d8-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="600d8-118">-Name</span></span>
<span data-ttu-id="600d8-119">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="600d8-119">Azure data share name</span></span>

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

### <span data-ttu-id="600d8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="600d8-120">-ResourceGroupName</span></span>
<span data-ttu-id="600d8-121">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="600d8-121">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="600d8-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="600d8-122">-TermsOfUse</span></span>
<span data-ttu-id="600d8-123">Condizioni per l'uso della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="600d8-123">Terms of use for azure data share</span></span>

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

### <span data-ttu-id="600d8-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="600d8-124">-Confirm</span></span>
<span data-ttu-id="600d8-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="600d8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="600d8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="600d8-126">-WhatIf</span></span>
<span data-ttu-id="600d8-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="600d8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="600d8-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="600d8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="600d8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="600d8-129">CommonParameters</span></span>
<span data-ttu-id="600d8-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="600d8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="600d8-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="600d8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="600d8-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="600d8-132">INPUTS</span></span>

### <span data-ttu-id="600d8-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="600d8-133">None</span></span>

## <span data-ttu-id="600d8-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="600d8-134">OUTPUTS</span></span>

### <span data-ttu-id="600d8-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="600d8-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="600d8-136">Note</span><span class="sxs-lookup"><span data-stu-id="600d8-136">NOTES</span></span>

## <span data-ttu-id="600d8-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="600d8-137">RELATED LINKS</span></span>
