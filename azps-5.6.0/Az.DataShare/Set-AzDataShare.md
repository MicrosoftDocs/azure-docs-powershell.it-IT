---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: ea159b52de0dd7d30c898f5119bc819c94d418fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966525"
---
# <span data-ttu-id="372f6-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="372f6-101">Set-AzDataShare</span></span>

## <span data-ttu-id="372f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="372f6-102">SYNOPSIS</span></span>
<span data-ttu-id="372f6-103">Aggiorna una condivisione dati esistente</span><span class="sxs-lookup"><span data-stu-id="372f6-103">Updates an existing data share</span></span>

## <span data-ttu-id="372f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="372f6-104">SYNTAX</span></span>

### <span data-ttu-id="372f6-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="372f6-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="372f6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="372f6-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="372f6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="372f6-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="372f6-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="372f6-108">DESCRIPTION</span></span>
<span data-ttu-id="372f6-109">Il cmdlet **Set-AzDataShare** aggiorna una condivisione dati esistente in un account di condivisione dati azure specificato.</span><span class="sxs-lookup"><span data-stu-id="372f6-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="372f6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="372f6-110">EXAMPLES</span></span>

### <span data-ttu-id="372f6-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="372f6-111">Example 1</span></span>
```
PS C:\> Set-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -Description "Updated description" -TermsOfUse "Updated terms"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Updated description
ProvisioningState   : Succeeded
Terms               : Updated terms
```

<span data-ttu-id="372f6-112">Questo comando aggiorna una condivisione dati esistente denominata AdsShare</span><span class="sxs-lookup"><span data-stu-id="372f6-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="372f6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="372f6-113">PARAMETERS</span></span>

### <span data-ttu-id="372f6-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="372f6-114">-AccountName</span></span>
<span data-ttu-id="372f6-115">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="372f6-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="372f6-116">-DefaultProfile</span></span>
<span data-ttu-id="372f6-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="372f6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="372f6-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="372f6-118">-Description</span></span>
<span data-ttu-id="372f6-119">Descrizione della condivisione dati</span><span class="sxs-lookup"><span data-stu-id="372f6-119">Description of Data Share</span></span>

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

### <span data-ttu-id="372f6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="372f6-120">-InputObject</span></span>
<span data-ttu-id="372f6-121">Oggetto di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="372f6-121">Azure data share object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="372f6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="372f6-122">-Name</span></span>
<span data-ttu-id="372f6-123">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="372f6-123">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372f6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="372f6-124">-ResourceGroupName</span></span>
<span data-ttu-id="372f6-125">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="372f6-125">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372f6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="372f6-126">-ResourceId</span></span>
<span data-ttu-id="372f6-127">ID risorsa della condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="372f6-127">The resource id of the azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="372f6-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="372f6-128">-TermsOfUse</span></span>
<span data-ttu-id="372f6-129">Condizioni per l'utilizzo per la condivisione dei dati</span><span class="sxs-lookup"><span data-stu-id="372f6-129">Terms of Use for Data Share</span></span>

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

### <span data-ttu-id="372f6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="372f6-130">-Confirm</span></span>
<span data-ttu-id="372f6-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="372f6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="372f6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="372f6-132">-WhatIf</span></span>
<span data-ttu-id="372f6-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="372f6-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="372f6-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="372f6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="372f6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="372f6-135">CommonParameters</span></span>
<span data-ttu-id="372f6-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="372f6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="372f6-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="372f6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="372f6-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="372f6-138">INPUTS</span></span>

### <span data-ttu-id="372f6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="372f6-139">System.String</span></span>

### <span data-ttu-id="372f6-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="372f6-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="372f6-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="372f6-141">OUTPUTS</span></span>

### <span data-ttu-id="372f6-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="372f6-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="372f6-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="372f6-143">NOTES</span></span>

## <span data-ttu-id="372f6-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="372f6-144">RELATED LINKS</span></span>
