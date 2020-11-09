---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: 69d44ea88b34aba027933cb3015a203bf06070fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297361"
---
# <span data-ttu-id="10a63-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="10a63-101">Set-AzDataShare</span></span>

## <span data-ttu-id="10a63-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="10a63-102">SYNOPSIS</span></span>
<span data-ttu-id="10a63-103">Aggiorna una condivisione dati esistente</span><span class="sxs-lookup"><span data-stu-id="10a63-103">Updates an existing data share</span></span>

## <span data-ttu-id="10a63-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10a63-104">SYNTAX</span></span>

### <span data-ttu-id="10a63-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="10a63-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10a63-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10a63-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10a63-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10a63-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10a63-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10a63-108">DESCRIPTION</span></span>
<span data-ttu-id="10a63-109">Il cmdlet **set-AzDataShare** aggiorna una condivisione di dati che esiste all'interno di un account di condivisione dati Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="10a63-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="10a63-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10a63-110">EXAMPLES</span></span>

### <span data-ttu-id="10a63-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="10a63-111">Example 1</span></span>
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

<span data-ttu-id="10a63-112">Questo comando aggiorna una condivisione dati esistente denominata AdsShare</span><span class="sxs-lookup"><span data-stu-id="10a63-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="10a63-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="10a63-113">PARAMETERS</span></span>

### <span data-ttu-id="10a63-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="10a63-114">-AccountName</span></span>
<span data-ttu-id="10a63-115">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="10a63-115">Azure data share account name</span></span>

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

### <span data-ttu-id="10a63-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10a63-116">-DefaultProfile</span></span>
<span data-ttu-id="10a63-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="10a63-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10a63-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="10a63-118">-Description</span></span>
<span data-ttu-id="10a63-119">Descrizione della condivisione dati</span><span class="sxs-lookup"><span data-stu-id="10a63-119">Description of Data Share</span></span>

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

### <span data-ttu-id="10a63-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10a63-120">-InputObject</span></span>
<span data-ttu-id="10a63-121">Oggetto condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="10a63-121">Azure data share object</span></span>


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

### <span data-ttu-id="10a63-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="10a63-122">-Name</span></span>
<span data-ttu-id="10a63-123">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="10a63-123">Azure data share name</span></span>

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

### <span data-ttu-id="10a63-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10a63-124">-ResourceGroupName</span></span>
<span data-ttu-id="10a63-125">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="10a63-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="10a63-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10a63-126">-ResourceId</span></span>
<span data-ttu-id="10a63-127">ID risorsa della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="10a63-127">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="10a63-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="10a63-128">-TermsOfUse</span></span>
<span data-ttu-id="10a63-129">Condizioni per l'uso della condivisione dati</span><span class="sxs-lookup"><span data-stu-id="10a63-129">Terms of Use for Data Share</span></span>

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

### <span data-ttu-id="10a63-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="10a63-130">-Confirm</span></span>
<span data-ttu-id="10a63-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10a63-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10a63-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10a63-132">-WhatIf</span></span>
<span data-ttu-id="10a63-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10a63-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10a63-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10a63-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10a63-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10a63-135">CommonParameters</span></span>
<span data-ttu-id="10a63-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10a63-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10a63-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10a63-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10a63-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="10a63-138">INPUTS</span></span>

### <span data-ttu-id="10a63-139">System. String</span><span class="sxs-lookup"><span data-stu-id="10a63-139">System.String</span></span>

### <span data-ttu-id="10a63-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="10a63-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="10a63-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10a63-141">OUTPUTS</span></span>

### <span data-ttu-id="10a63-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="10a63-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="10a63-143">Note</span><span class="sxs-lookup"><span data-stu-id="10a63-143">NOTES</span></span>

## <span data-ttu-id="10a63-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10a63-144">RELATED LINKS</span></span>
