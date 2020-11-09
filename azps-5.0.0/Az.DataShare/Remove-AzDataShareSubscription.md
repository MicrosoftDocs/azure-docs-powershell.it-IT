---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: eb2b7f1e22ff3d2fccdff0d84a77f5c68ca8e70d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297385"
---
# <span data-ttu-id="5861a-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="5861a-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="5861a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5861a-102">SYNOPSIS</span></span>
<span data-ttu-id="5861a-103">Rimuove un abbonamento a una condivisione</span><span class="sxs-lookup"><span data-stu-id="5861a-103">removes a share subscription</span></span>

## <span data-ttu-id="5861a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5861a-104">SYNTAX</span></span>

### <span data-ttu-id="5861a-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5861a-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5861a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5861a-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5861a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5861a-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5861a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5861a-108">DESCRIPTION</span></span>
<span data-ttu-id="5861a-109">Il cmdlet **Remove-AzDataShareSubscription** rimuove un abbonamento a una condivisione</span><span class="sxs-lookup"><span data-stu-id="5861a-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="5861a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5861a-110">EXAMPLES</span></span>

### <span data-ttu-id="5861a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5861a-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="5861a-112">Questo comando rimuove un sharesubscription denominato AdsShareSubscription dall'account WikiAds.</span><span class="sxs-lookup"><span data-stu-id="5861a-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="5861a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5861a-113">PARAMETERS</span></span>

### <span data-ttu-id="5861a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5861a-114">-AccountName</span></span>
<span data-ttu-id="5861a-115">Nome dell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="5861a-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="5861a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5861a-116">-AsJob</span></span>
<span data-ttu-id="5861a-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="5861a-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="5861a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5861a-118">-DefaultProfile</span></span>
<span data-ttu-id="5861a-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5861a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5861a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5861a-120">-InputObject</span></span>
<span data-ttu-id="5861a-121">Oggetto abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="5861a-121">Azure data share subscription object</span></span>


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

### <span data-ttu-id="5861a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5861a-122">-Name</span></span>
<span data-ttu-id="5861a-123">Nome dell'abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="5861a-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="5861a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5861a-124">-PassThru</span></span>
<span data-ttu-id="5861a-125">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="5861a-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="5861a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5861a-126">-ResourceGroupName</span></span>
<span data-ttu-id="5861a-127">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="5861a-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="5861a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5861a-128">-ResourceId</span></span>
<span data-ttu-id="5861a-129">ID risorsa dell'abbonamento a una condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="5861a-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="5861a-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5861a-130">-Confirm</span></span>
<span data-ttu-id="5861a-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5861a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5861a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5861a-132">-WhatIf</span></span>
<span data-ttu-id="5861a-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5861a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5861a-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5861a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5861a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5861a-135">CommonParameters</span></span>
<span data-ttu-id="5861a-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5861a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5861a-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5861a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5861a-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5861a-138">INPUTS</span></span>

### <span data-ttu-id="5861a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5861a-139">System.String</span></span>

### <span data-ttu-id="5861a-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="5861a-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="5861a-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5861a-141">OUTPUTS</span></span>

### <span data-ttu-id="5861a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5861a-142">System.Boolean</span></span>

## <span data-ttu-id="5861a-143">Note</span><span class="sxs-lookup"><span data-stu-id="5861a-143">NOTES</span></span>

## <span data-ttu-id="5861a-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5861a-144">RELATED LINKS</span></span>
