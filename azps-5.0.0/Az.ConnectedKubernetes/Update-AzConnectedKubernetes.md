---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/update-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
ms.openlocfilehash: 2913a4288bad6c1cb8c908d80b8c751a08483a8b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200212"
---
# <span data-ttu-id="bcac0-101">Update-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="bcac0-101">Update-AzConnectedKubernetes</span></span>

## <span data-ttu-id="bcac0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bcac0-102">SYNOPSIS</span></span>
<span data-ttu-id="bcac0-103">API per aggiornare determinate proprietà della risorsa cluster connessa</span><span class="sxs-lookup"><span data-stu-id="bcac0-103">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="bcac0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcac0-104">SYNTAX</span></span>

### <span data-ttu-id="bcac0-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bcac0-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bcac0-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="bcac0-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bcac0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcac0-107">DESCRIPTION</span></span>
<span data-ttu-id="bcac0-108">API per aggiornare determinate proprietà della risorsa cluster connessa</span><span class="sxs-lookup"><span data-stu-id="bcac0-108">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="bcac0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcac0-109">EXAMPLES</span></span>

### <span data-ttu-id="bcac0-110">Esempio 1: aggiornare un kubernetes connesso</span><span class="sxs-lookup"><span data-stu-id="bcac0-110">Example 1: Update a connected kubernetes</span></span>
```powershell
PS C:\> Update-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t01 -Tag @{'key'='1'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="bcac0-111">Questo comando aggiorna un kubernetes connesso.</span><span class="sxs-lookup"><span data-stu-id="bcac0-111">This command updates a connected kubernetes.</span></span>

### <span data-ttu-id="bcac0-112">Esempio 2: aggiornare un kubernetes connesso per oggetto</span><span class="sxs-lookup"><span data-stu-id="bcac0-112">Example 2: Update a connected kubernetes by object</span></span>
```powershell
PS C:\> $conn = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t03
PS C:\> Update-AzConnectedKubernetes -InputObject $conn -Tag @{'key'='2'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t03 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="bcac0-113">Questo comando aggiorna un kubernetes connesso per oggetto.</span><span class="sxs-lookup"><span data-stu-id="bcac0-113">This command updates a connected kubernetes by object.</span></span>

## <span data-ttu-id="bcac0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bcac0-114">PARAMETERS</span></span>

### <span data-ttu-id="bcac0-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="bcac0-115">-ClusterName</span></span>
<span data-ttu-id="bcac0-116">Nome del cluster Kubernetes in cui viene chiamato Get.</span><span class="sxs-lookup"><span data-stu-id="bcac0-116">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="bcac0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcac0-117">-DefaultProfile</span></span>
<span data-ttu-id="bcac0-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bcac0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcac0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcac0-119">-InputObject</span></span>
<span data-ttu-id="bcac0-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="bcac0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bcac0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcac0-121">-ResourceGroupName</span></span>
<span data-ttu-id="bcac0-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bcac0-122">The name of the resource group.</span></span>
<span data-ttu-id="bcac0-123">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="bcac0-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bcac0-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bcac0-124">-SubscriptionId</span></span>
<span data-ttu-id="bcac0-125">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bcac0-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bcac0-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="bcac0-126">-Tag</span></span>
<span data-ttu-id="bcac0-127">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="bcac0-127">Resource tags.</span></span>

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

### <span data-ttu-id="bcac0-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bcac0-128">-Confirm</span></span>
<span data-ttu-id="bcac0-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcac0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcac0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcac0-130">-WhatIf</span></span>
<span data-ttu-id="bcac0-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcac0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcac0-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcac0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcac0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcac0-133">CommonParameters</span></span>
<span data-ttu-id="bcac0-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcac0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcac0-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bcac0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcac0-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bcac0-136">INPUTS</span></span>

### <span data-ttu-id="bcac0-137">Microsoft. Azure. PowerShell. Cmdlets. ConnectedKubernetes. Models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="bcac0-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="bcac0-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcac0-138">OUTPUTS</span></span>

### <span data-ttu-id="bcac0-139">Microsoft. Azure. PowerShell. Cmdlets. ConnectedKubernetes. Models. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="bcac0-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="bcac0-140">Note</span><span class="sxs-lookup"><span data-stu-id="bcac0-140">NOTES</span></span>

<span data-ttu-id="bcac0-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bcac0-141">ALIASES</span></span>

<span data-ttu-id="bcac0-142">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bcac0-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bcac0-143">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="bcac0-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bcac0-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bcac0-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bcac0-145">INPUTOBJECT <IConnectedKubernetesIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="bcac0-145">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bcac0-146">`[ClusterName <String>]`: Nome del cluster Kubernetes in cui viene chiamato Get.</span><span class="sxs-lookup"><span data-stu-id="bcac0-146">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="bcac0-147">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="bcac0-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bcac0-148">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bcac0-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bcac0-149">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="bcac0-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="bcac0-150">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bcac0-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="bcac0-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcac0-151">RELATED LINKS</span></span>
