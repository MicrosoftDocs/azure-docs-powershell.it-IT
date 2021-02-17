---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: 69d44ea88b34aba027933cb3015a203bf06070fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194551"
---
# <span data-ttu-id="7d196-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="7d196-101">Set-AzDataShare</span></span>

## <span data-ttu-id="7d196-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d196-102">SYNOPSIS</span></span>
<span data-ttu-id="7d196-103">Aggiorna una condivisione dati esistente</span><span class="sxs-lookup"><span data-stu-id="7d196-103">Updates an existing data share</span></span>

## <span data-ttu-id="7d196-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d196-104">SYNTAX</span></span>

### <span data-ttu-id="7d196-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7d196-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d196-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d196-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d196-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d196-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d196-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7d196-108">DESCRIPTION</span></span>
<span data-ttu-id="7d196-109">Il cmdlet **Set-AzDataShare** aggiorna una condivisione dati esistente in un account di condivisione dati azure specificato.</span><span class="sxs-lookup"><span data-stu-id="7d196-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="7d196-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d196-110">EXAMPLES</span></span>

### <span data-ttu-id="7d196-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7d196-111">Example 1</span></span>
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

<span data-ttu-id="7d196-112">Questo comando aggiorna una condivisione dati esistente denominata AdsShare</span><span class="sxs-lookup"><span data-stu-id="7d196-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="7d196-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d196-113">PARAMETERS</span></span>

### <span data-ttu-id="7d196-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7d196-114">-AccountName</span></span>
<span data-ttu-id="7d196-115">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="7d196-115">Azure data share account name</span></span>

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

### <span data-ttu-id="7d196-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d196-116">-DefaultProfile</span></span>
<span data-ttu-id="7d196-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d196-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d196-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d196-118">-Description</span></span>
<span data-ttu-id="7d196-119">Descrizione della condivisione dati</span><span class="sxs-lookup"><span data-stu-id="7d196-119">Description of Data Share</span></span>

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

### <span data-ttu-id="7d196-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d196-120">-InputObject</span></span>
<span data-ttu-id="7d196-121">Oggetto di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="7d196-121">Azure data share object</span></span>


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

### <span data-ttu-id="7d196-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7d196-122">-Name</span></span>
<span data-ttu-id="7d196-123">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="7d196-123">Azure data share name</span></span>

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

### <span data-ttu-id="7d196-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d196-124">-ResourceGroupName</span></span>
<span data-ttu-id="7d196-125">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="7d196-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="7d196-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d196-126">-ResourceId</span></span>
<span data-ttu-id="7d196-127">ID risorsa della condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="7d196-127">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="7d196-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="7d196-128">-TermsOfUse</span></span>
<span data-ttu-id="7d196-129">Condizioni per l'utilizzo per la condivisione dei dati</span><span class="sxs-lookup"><span data-stu-id="7d196-129">Terms of Use for Data Share</span></span>

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

### <span data-ttu-id="7d196-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d196-130">-Confirm</span></span>
<span data-ttu-id="7d196-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d196-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d196-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d196-132">-WhatIf</span></span>
<span data-ttu-id="7d196-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d196-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d196-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d196-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d196-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d196-135">CommonParameters</span></span>
<span data-ttu-id="7d196-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d196-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d196-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7d196-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d196-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="7d196-138">INPUTS</span></span>

### <span data-ttu-id="7d196-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7d196-139">System.String</span></span>

### <span data-ttu-id="7d196-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="7d196-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="7d196-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d196-141">OUTPUTS</span></span>

### <span data-ttu-id="7d196-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="7d196-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="7d196-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="7d196-143">NOTES</span></span>

## <span data-ttu-id="7d196-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d196-144">RELATED LINKS</span></span>
