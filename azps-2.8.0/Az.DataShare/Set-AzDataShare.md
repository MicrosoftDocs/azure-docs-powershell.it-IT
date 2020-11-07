---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: f10aaca629519d40334aabdac604531b726edd69
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674638"
---
# <span data-ttu-id="32dfb-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="32dfb-101">Set-AzDataShare</span></span>

## <span data-ttu-id="32dfb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="32dfb-103">Aggiorna una condivisione dati esistente</span><span class="sxs-lookup"><span data-stu-id="32dfb-103">Updates an existing data share</span></span>

## <span data-ttu-id="32dfb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32dfb-104">SYNTAX</span></span>

### <span data-ttu-id="32dfb-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="32dfb-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32dfb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32dfb-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32dfb-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32dfb-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32dfb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32dfb-108">DESCRIPTION</span></span>
<span data-ttu-id="32dfb-109">Il cmdlet **set-AzDataShare** aggiorna una condivisione di dati che esiste all'interno di un account di condivisione dati Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="32dfb-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="32dfb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32dfb-110">EXAMPLES</span></span>

### <span data-ttu-id="32dfb-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="32dfb-111">Example 1</span></span>
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

<span data-ttu-id="32dfb-112">Questo comando aggiorna una condivisione dati esistente denominata AdsShare</span><span class="sxs-lookup"><span data-stu-id="32dfb-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="32dfb-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32dfb-113">PARAMETERS</span></span>

### <span data-ttu-id="32dfb-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="32dfb-114">-AccountName</span></span>
<span data-ttu-id="32dfb-115">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="32dfb-115">Azure data share account name</span></span>

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

### <span data-ttu-id="32dfb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32dfb-116">-DefaultProfile</span></span>
<span data-ttu-id="32dfb-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32dfb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32dfb-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="32dfb-118">-Description</span></span>
<span data-ttu-id="32dfb-119">Descrizione della condivisione dati</span><span class="sxs-lookup"><span data-stu-id="32dfb-119">Description of Data Share</span></span>

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

### <span data-ttu-id="32dfb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32dfb-120">-InputObject</span></span>
<span data-ttu-id="32dfb-121">Oggetto condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="32dfb-121">Azure data share object</span></span>


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

### <span data-ttu-id="32dfb-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="32dfb-122">-Name</span></span>
<span data-ttu-id="32dfb-123">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="32dfb-123">Azure data share name</span></span>

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

### <span data-ttu-id="32dfb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32dfb-124">-ResourceGroupName</span></span>
<span data-ttu-id="32dfb-125">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="32dfb-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="32dfb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32dfb-126">-ResourceId</span></span>
<span data-ttu-id="32dfb-127">ID risorsa della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="32dfb-127">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="32dfb-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="32dfb-128">-TermsOfUse</span></span>
<span data-ttu-id="32dfb-129">Condizioni per l'uso della condivisione dati</span><span class="sxs-lookup"><span data-stu-id="32dfb-129">Terms of Use for Data Share</span></span>

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

### <span data-ttu-id="32dfb-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="32dfb-130">-Confirm</span></span>
<span data-ttu-id="32dfb-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32dfb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32dfb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32dfb-132">-WhatIf</span></span>
<span data-ttu-id="32dfb-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32dfb-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32dfb-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32dfb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32dfb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32dfb-135">CommonParameters</span></span>
<span data-ttu-id="32dfb-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32dfb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32dfb-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32dfb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32dfb-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32dfb-138">INPUTS</span></span>

### <span data-ttu-id="32dfb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="32dfb-139">System.String</span></span>

### <span data-ttu-id="32dfb-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="32dfb-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="32dfb-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32dfb-141">OUTPUTS</span></span>

### <span data-ttu-id="32dfb-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="32dfb-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="32dfb-143">Note</span><span class="sxs-lookup"><span data-stu-id="32dfb-143">NOTES</span></span>

## <span data-ttu-id="32dfb-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32dfb-144">RELATED LINKS</span></span>
