---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: 265f917068237fee13f77eb8c87e0adf8cd12f08
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324402"
---
# <span data-ttu-id="5e0de-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="5e0de-101">New-AzDataShare</span></span>

## <span data-ttu-id="5e0de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e0de-102">SYNOPSIS</span></span>
<span data-ttu-id="5e0de-103">Crea una condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="5e0de-103">Creates a azure data share.</span></span>

## <span data-ttu-id="5e0de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e0de-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e0de-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e0de-105">DESCRIPTION</span></span>
<span data-ttu-id="5e0de-106">Il cmdlet **New-AzDataShare** crea una condivisione dati all'interno di un account di condivisione dati di Azure specificato fornendo il nome del gruppo di risorse, il nome dell'account, il nome della condivisione e il tipo di condivisione.</span><span class="sxs-lookup"><span data-stu-id="5e0de-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="5e0de-107">Descrizione e condizioni per l'uso sono parametri facoltativi che possono essere impostati durante la creazione della condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="5e0de-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="5e0de-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e0de-108">EXAMPLES</span></span>

### <span data-ttu-id="5e0de-109">Esempio 1: creare una condivisione dati</span><span class="sxs-lookup"><span data-stu-id="5e0de-109">Example 1 : Create a data share</span></span>
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

<span data-ttu-id="5e0de-110">Questo comando crea una condivisione dati denominata AdsShare di tipo CopyBased nell'account di condivisione dati WikiAdsAccount in annunci gruppo risorse con descrizione e condizioni per l'uso.</span><span class="sxs-lookup"><span data-stu-id="5e0de-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="5e0de-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e0de-111">PARAMETERS</span></span>

### <span data-ttu-id="5e0de-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5e0de-112">-AccountName</span></span>
<span data-ttu-id="5e0de-113">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="5e0de-113">Azure data share account name</span></span>

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

### <span data-ttu-id="5e0de-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e0de-114">-DefaultProfile</span></span>
<span data-ttu-id="5e0de-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e0de-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e0de-116">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e0de-116">-Description</span></span>
<span data-ttu-id="5e0de-117">Descrizione della condivisione di dati di Azure</span><span class="sxs-lookup"><span data-stu-id="5e0de-117">Description of azure data share</span></span>

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

### <span data-ttu-id="5e0de-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e0de-118">-Name</span></span>
<span data-ttu-id="5e0de-119">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="5e0de-119">Azure data share name</span></span>

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

### <span data-ttu-id="5e0de-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e0de-120">-ResourceGroupName</span></span>
<span data-ttu-id="5e0de-121">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="5e0de-121">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="5e0de-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="5e0de-122">-TermsOfUse</span></span>
<span data-ttu-id="5e0de-123">Condizioni per l'uso della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="5e0de-123">Terms of use for azure data share</span></span>

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

### <span data-ttu-id="5e0de-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5e0de-124">-Confirm</span></span>
<span data-ttu-id="5e0de-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e0de-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e0de-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e0de-126">-WhatIf</span></span>
<span data-ttu-id="5e0de-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e0de-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e0de-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e0de-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e0de-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e0de-129">CommonParameters</span></span>
<span data-ttu-id="5e0de-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e0de-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e0de-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e0de-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e0de-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e0de-132">INPUTS</span></span>

### <span data-ttu-id="5e0de-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5e0de-133">None</span></span>

## <span data-ttu-id="5e0de-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e0de-134">OUTPUTS</span></span>

### <span data-ttu-id="5e0de-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="5e0de-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="5e0de-136">Note</span><span class="sxs-lookup"><span data-stu-id="5e0de-136">NOTES</span></span>

## <span data-ttu-id="5e0de-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e0de-137">RELATED LINKS</span></span>
