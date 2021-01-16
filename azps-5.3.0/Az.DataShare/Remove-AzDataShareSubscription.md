---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: eb2b7f1e22ff3d2fccdff0d84a77f5c68ca8e70d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377103"
---
# <span data-ttu-id="a491e-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="a491e-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="a491e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a491e-102">SYNOPSIS</span></span>
<span data-ttu-id="a491e-103">Rimuove un abbonamento a una condivisione</span><span class="sxs-lookup"><span data-stu-id="a491e-103">removes a share subscription</span></span>

## <span data-ttu-id="a491e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a491e-104">SYNTAX</span></span>

### <span data-ttu-id="a491e-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a491e-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a491e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a491e-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a491e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a491e-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a491e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a491e-108">DESCRIPTION</span></span>
<span data-ttu-id="a491e-109">Il cmdlet **Remove-AzDataShareSubscription** rimuove un abbonamento a una condivisione</span><span class="sxs-lookup"><span data-stu-id="a491e-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="a491e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a491e-110">EXAMPLES</span></span>

### <span data-ttu-id="a491e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a491e-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="a491e-112">Questo comando rimuove un sharesubscription denominato AdsShareSubscription dall'account WikiAds.</span><span class="sxs-lookup"><span data-stu-id="a491e-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="a491e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a491e-113">PARAMETERS</span></span>

### <span data-ttu-id="a491e-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a491e-114">-AccountName</span></span>
<span data-ttu-id="a491e-115">Nome dell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="a491e-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="a491e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a491e-116">-AsJob</span></span>
<span data-ttu-id="a491e-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="a491e-117">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a491e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a491e-118">-DefaultProfile</span></span>
<span data-ttu-id="a491e-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a491e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a491e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a491e-120">-InputObject</span></span>
<span data-ttu-id="a491e-121">Oggetto abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="a491e-121">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a491e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a491e-122">-Name</span></span>
<span data-ttu-id="a491e-123">Nome dell'abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="a491e-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="a491e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a491e-124">-PassThru</span></span>
<span data-ttu-id="a491e-125">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="a491e-125">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a491e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a491e-126">-ResourceGroupName</span></span>
<span data-ttu-id="a491e-127">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="a491e-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="a491e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a491e-128">-ResourceId</span></span>
<span data-ttu-id="a491e-129">ID risorsa dell'abbonamento a una condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="a491e-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="a491e-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a491e-130">-Confirm</span></span>
<span data-ttu-id="a491e-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a491e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a491e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a491e-132">-WhatIf</span></span>
<span data-ttu-id="a491e-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a491e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a491e-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a491e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a491e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a491e-135">CommonParameters</span></span>
<span data-ttu-id="a491e-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a491e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a491e-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a491e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a491e-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a491e-138">INPUTS</span></span>

### <span data-ttu-id="a491e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a491e-139">System.String</span></span>

### <span data-ttu-id="a491e-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="a491e-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="a491e-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a491e-141">OUTPUTS</span></span>

### <span data-ttu-id="a491e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a491e-142">System.Boolean</span></span>

## <span data-ttu-id="a491e-143">Note</span><span class="sxs-lookup"><span data-stu-id="a491e-143">NOTES</span></span>

## <span data-ttu-id="a491e-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a491e-144">RELATED LINKS</span></span>
