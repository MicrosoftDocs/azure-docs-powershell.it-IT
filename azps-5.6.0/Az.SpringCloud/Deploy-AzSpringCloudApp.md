---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: 96b3b3fcb2fcea50e1607c67d98079e5d1600f4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955326"
---
# <span data-ttu-id="6d658-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="6d658-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="6d658-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d658-102">SYNOPSIS</span></span>
<span data-ttu-id="6d658-103">Distribuire il jar incorporato al servizio.</span><span class="sxs-lookup"><span data-stu-id="6d658-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="6d658-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d658-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="6d658-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6d658-105">DESCRIPTION</span></span>
<span data-ttu-id="6d658-106">Distribuire il jar incorporato al servizio.</span><span class="sxs-lookup"><span data-stu-id="6d658-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="6d658-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d658-107">EXAMPLES</span></span>

### <span data-ttu-id="6d658-108">Esempio 1: Distribuire il jar compilato locale nel servizio in base al nome.</span><span class="sxs-lookup"><span data-stu-id="6d658-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="6d658-109">Distribuire il jar compilato locale al servizio in base al nome.</span><span class="sxs-lookup"><span data-stu-id="6d658-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="6d658-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d658-110">PARAMETERS</span></span>

### <span data-ttu-id="6d658-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d658-111">-AsJob</span></span>
<span data-ttu-id="6d658-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="6d658-112">Run the command as a job</span></span>

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

### <span data-ttu-id="6d658-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d658-113">-DefaultProfile</span></span>
<span data-ttu-id="6d658-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d658-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d658-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="6d658-115">-JarPath</span></span>
<span data-ttu-id="6d658-116">Il percorso del barattolo deve essere ammortidato.</span><span class="sxs-lookup"><span data-stu-id="6d658-116">The path of the jar need to be deploied.</span></span>

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

### <span data-ttu-id="6d658-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6d658-117">-Name</span></span>
<span data-ttu-id="6d658-118">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="6d658-118">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d658-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6d658-119">-NoWait</span></span>
<span data-ttu-id="6d658-120">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="6d658-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6d658-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d658-121">-ResourceGroupName</span></span>
<span data-ttu-id="6d658-122">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6d658-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6d658-123">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="6d658-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6d658-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6d658-124">-ServiceName</span></span>
<span data-ttu-id="6d658-125">Nome della risorsa Servizio.</span><span class="sxs-lookup"><span data-stu-id="6d658-125">The name of the Service resource.</span></span>

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

### <span data-ttu-id="6d658-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d658-126">-SubscriptionId</span></span>
<span data-ttu-id="6d658-127">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6d658-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6d658-128">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="6d658-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d658-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d658-129">-Confirm</span></span>
<span data-ttu-id="6d658-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d658-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d658-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d658-131">-WhatIf</span></span>
<span data-ttu-id="6d658-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d658-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d658-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d658-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d658-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d658-134">CommonParameters</span></span>
<span data-ttu-id="6d658-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d658-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d658-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6d658-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d658-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="6d658-137">INPUTS</span></span>

## <span data-ttu-id="6d658-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d658-138">OUTPUTS</span></span>

### <span data-ttu-id="6d658-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="6d658-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="6d658-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="6d658-140">NOTES</span></span>

<span data-ttu-id="6d658-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6d658-141">ALIASES</span></span>

## <span data-ttu-id="6d658-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d658-142">RELATED LINKS</span></span>

