---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: c92348e32247bfed0b3aa7ce59b4772f7d3ef4af
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022375"
---
# <span data-ttu-id="16dc9-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="16dc9-101">Set-AzDataShare</span></span>

## <span data-ttu-id="16dc9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16dc9-102">SYNOPSIS</span></span>
<span data-ttu-id="16dc9-103">Aggiorna una condivisione dati esistente</span><span class="sxs-lookup"><span data-stu-id="16dc9-103">Updates an existing data share</span></span>

## <span data-ttu-id="16dc9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16dc9-104">SYNTAX</span></span>

### <span data-ttu-id="16dc9-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="16dc9-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16dc9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16dc9-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16dc9-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16dc9-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16dc9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16dc9-108">DESCRIPTION</span></span>
<span data-ttu-id="16dc9-109">Il cmdlet **set-AzDataShare** aggiorna una condivisione di dati che esiste all'interno di un account di condivisione dati Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="16dc9-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="16dc9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16dc9-110">EXAMPLES</span></span>

### <span data-ttu-id="16dc9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="16dc9-111">Example 1</span></span>
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

<span data-ttu-id="16dc9-112">Questo comando aggiorna una condivisione dati esistente denominata AdsShare</span><span class="sxs-lookup"><span data-stu-id="16dc9-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="16dc9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16dc9-113">PARAMETERS</span></span>

### <span data-ttu-id="16dc9-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="16dc9-114">-AccountName</span></span>
<span data-ttu-id="16dc9-115">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="16dc9-115">Azure data share account name</span></span>

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

### <span data-ttu-id="16dc9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16dc9-116">-DefaultProfile</span></span>
<span data-ttu-id="16dc9-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16dc9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16dc9-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="16dc9-118">-Description</span></span>
<span data-ttu-id="16dc9-119">Descrizione della condivisione dati</span><span class="sxs-lookup"><span data-stu-id="16dc9-119">Description of Data Share</span></span>

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

### <span data-ttu-id="16dc9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16dc9-120">-InputObject</span></span>
<span data-ttu-id="16dc9-121">Oggetto condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="16dc9-121">Azure data share object</span></span>


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

### <span data-ttu-id="16dc9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="16dc9-122">-Name</span></span>
<span data-ttu-id="16dc9-123">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="16dc9-123">Azure data share name</span></span>

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

### <span data-ttu-id="16dc9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16dc9-124">-ResourceGroupName</span></span>
<span data-ttu-id="16dc9-125">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="16dc9-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="16dc9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16dc9-126">-ResourceId</span></span>
<span data-ttu-id="16dc9-127">ID risorsa della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="16dc9-127">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="16dc9-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="16dc9-128">-TermsOfUse</span></span>
<span data-ttu-id="16dc9-129">Condizioni per l'uso della condivisione dati</span><span class="sxs-lookup"><span data-stu-id="16dc9-129">Terms of Use for Data Share</span></span>

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

### <span data-ttu-id="16dc9-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="16dc9-130">-Confirm</span></span>
<span data-ttu-id="16dc9-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16dc9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16dc9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16dc9-132">-WhatIf</span></span>
<span data-ttu-id="16dc9-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16dc9-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16dc9-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16dc9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16dc9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16dc9-135">CommonParameters</span></span>
<span data-ttu-id="16dc9-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16dc9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16dc9-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16dc9-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16dc9-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16dc9-138">INPUTS</span></span>

### <span data-ttu-id="16dc9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="16dc9-139">System.String</span></span>

### <span data-ttu-id="16dc9-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="16dc9-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="16dc9-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16dc9-141">OUTPUTS</span></span>

### <span data-ttu-id="16dc9-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="16dc9-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="16dc9-143">Note</span><span class="sxs-lookup"><span data-stu-id="16dc9-143">NOTES</span></span>

## <span data-ttu-id="16dc9-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16dc9-144">RELATED LINKS</span></span>
