---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: 12298f5c61981cb34572a104d39a279f7024adf2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020824"
---
# <span data-ttu-id="eba04-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="eba04-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="eba04-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eba04-102">SYNOPSIS</span></span>
<span data-ttu-id="eba04-103">Rimuove un abbonamento a una condivisione</span><span class="sxs-lookup"><span data-stu-id="eba04-103">removes a share subscription</span></span>

## <span data-ttu-id="eba04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eba04-104">SYNTAX</span></span>

### <span data-ttu-id="eba04-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eba04-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eba04-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eba04-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eba04-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eba04-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eba04-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eba04-108">DESCRIPTION</span></span>
<span data-ttu-id="eba04-109">Il cmdlet **Remove-AzDataShareSubscription** rimuove un abbonamento a una condivisione</span><span class="sxs-lookup"><span data-stu-id="eba04-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="eba04-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eba04-110">EXAMPLES</span></span>

### <span data-ttu-id="eba04-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eba04-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="eba04-112">Questo comando rimuove un sharesubscription denominato AdsShareSubscription dall'account WikiAds.</span><span class="sxs-lookup"><span data-stu-id="eba04-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="eba04-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eba04-113">PARAMETERS</span></span>

### <span data-ttu-id="eba04-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eba04-114">-AccountName</span></span>
<span data-ttu-id="eba04-115">Nome dell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="eba04-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="eba04-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eba04-116">-AsJob</span></span>
<span data-ttu-id="eba04-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="eba04-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="eba04-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eba04-118">-DefaultProfile</span></span>
<span data-ttu-id="eba04-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eba04-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eba04-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eba04-120">-InputObject</span></span>
<span data-ttu-id="eba04-121">Oggetto abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="eba04-121">Azure data share subscription object</span></span>


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

### <span data-ttu-id="eba04-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="eba04-122">-Name</span></span>
<span data-ttu-id="eba04-123">Nome dell'abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="eba04-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="eba04-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eba04-124">-PassThru</span></span>
<span data-ttu-id="eba04-125">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="eba04-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="eba04-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eba04-126">-ResourceGroupName</span></span>
<span data-ttu-id="eba04-127">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="eba04-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="eba04-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eba04-128">-ResourceId</span></span>
<span data-ttu-id="eba04-129">ID risorsa dell'abbonamento a una condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="eba04-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="eba04-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="eba04-130">-Confirm</span></span>
<span data-ttu-id="eba04-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eba04-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eba04-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eba04-132">-WhatIf</span></span>
<span data-ttu-id="eba04-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eba04-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eba04-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eba04-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eba04-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eba04-135">CommonParameters</span></span>
<span data-ttu-id="eba04-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eba04-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eba04-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eba04-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eba04-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eba04-138">INPUTS</span></span>

### <span data-ttu-id="eba04-139">System. String</span><span class="sxs-lookup"><span data-stu-id="eba04-139">System.String</span></span>

### <span data-ttu-id="eba04-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="eba04-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="eba04-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eba04-141">OUTPUTS</span></span>

### <span data-ttu-id="eba04-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eba04-142">System.Boolean</span></span>

## <span data-ttu-id="eba04-143">Note</span><span class="sxs-lookup"><span data-stu-id="eba04-143">NOTES</span></span>

## <span data-ttu-id="eba04-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eba04-144">RELATED LINKS</span></span>
