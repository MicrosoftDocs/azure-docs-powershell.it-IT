---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/update-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
ms.openlocfilehash: 2e0c7f11592238f11f49e82102c6d58c24f8b9fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012445"
---
# <span data-ttu-id="d5306-101">Update-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="d5306-101">Update-AzConnectedKubernetes</span></span>

## <span data-ttu-id="d5306-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5306-102">SYNOPSIS</span></span>
<span data-ttu-id="d5306-103">API per aggiornare determinate proprietà della risorsa cluster connessa.</span><span class="sxs-lookup"><span data-stu-id="d5306-103">API to update certain properties of the connected cluster resource.</span></span>

## <span data-ttu-id="d5306-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5306-104">SYNTAX</span></span>

### <span data-ttu-id="d5306-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d5306-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d5306-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d5306-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d5306-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d5306-107">DESCRIPTION</span></span>
<span data-ttu-id="d5306-108">API per aggiornare determinate proprietà della risorsa cluster connessa.</span><span class="sxs-lookup"><span data-stu-id="d5306-108">API to update certain properties of the connected cluster resource.</span></span>

## <span data-ttu-id="d5306-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5306-109">EXAMPLES</span></span>

### <span data-ttu-id="d5306-110">Esempio 1: Aggiornare un kubernet connesso</span><span class="sxs-lookup"><span data-stu-id="d5306-110">Example 1: Update a connected kubernetes</span></span>
```powershell
PS C:\> Update-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t01 -Tag @{'key'='1'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="d5306-111">Questo comando aggiorna un kubernet connesso.</span><span class="sxs-lookup"><span data-stu-id="d5306-111">This command updates a connected kubernetes.</span></span>

### <span data-ttu-id="d5306-112">Esempio 2: Aggiornare un kubernet connesso in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="d5306-112">Example 2: Update a connected kubernetes by object</span></span>
```powershell
PS C:\> $conn = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t03
PS C:\> Update-AzConnectedKubernetes -InputObject $conn -Tag @{'key'='2'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t03 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="d5306-113">Questo comando aggiorna i kubernet connessi in base all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d5306-113">This command updates a connected kubernetes by object.</span></span>

## <span data-ttu-id="d5306-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5306-114">PARAMETERS</span></span>

### <span data-ttu-id="d5306-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d5306-115">-ClusterName</span></span>
<span data-ttu-id="d5306-116">Il nome del cluster Kubernetes su cui si chiama get.</span><span class="sxs-lookup"><span data-stu-id="d5306-116">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5306-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5306-117">-DefaultProfile</span></span>
<span data-ttu-id="d5306-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d5306-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5306-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5306-119">-InputObject</span></span>
<span data-ttu-id="d5306-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d5306-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5306-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5306-121">-ResourceGroupName</span></span>
<span data-ttu-id="d5306-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d5306-122">The name of the resource group.</span></span>
<span data-ttu-id="d5306-123">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d5306-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5306-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5306-124">-SubscriptionId</span></span>
<span data-ttu-id="d5306-125">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d5306-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5306-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="d5306-126">-Tag</span></span>
<span data-ttu-id="d5306-127">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="d5306-127">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5306-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5306-128">-Confirm</span></span>
<span data-ttu-id="d5306-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5306-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5306-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5306-130">-WhatIf</span></span>
<span data-ttu-id="d5306-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5306-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5306-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5306-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5306-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5306-133">CommonParameters</span></span>
<span data-ttu-id="d5306-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5306-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5306-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d5306-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5306-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="d5306-136">INPUTS</span></span>

### <span data-ttu-id="d5306-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="d5306-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="d5306-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5306-138">OUTPUTS</span></span>

### <span data-ttu-id="d5306-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="d5306-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span></span>

## <span data-ttu-id="d5306-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="d5306-140">NOTES</span></span>

<span data-ttu-id="d5306-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d5306-141">ALIASES</span></span>

<span data-ttu-id="d5306-142">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="d5306-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d5306-143">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d5306-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d5306-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d5306-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d5306-145">INPUTOBJECT <IConnectedKubernetesIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="d5306-145">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d5306-146">`[ClusterName <String>]`: il nome del cluster Kubernetes su cui si chiama get.</span><span class="sxs-lookup"><span data-stu-id="d5306-146">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="d5306-147">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="d5306-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d5306-148">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d5306-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d5306-149">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d5306-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="d5306-150">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d5306-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="d5306-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5306-151">RELATED LINKS</span></span>

