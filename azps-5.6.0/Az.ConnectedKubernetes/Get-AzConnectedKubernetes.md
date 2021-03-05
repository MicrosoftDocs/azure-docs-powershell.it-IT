---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: da4cd54b9865cdf30487a7e49e5581474ebb2a35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012526"
---
# <span data-ttu-id="a4fdd-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="a4fdd-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="a4fdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4fdd-102">SYNOPSIS</span></span>
<span data-ttu-id="a4fdd-103">Restituisce le proprietà del cluster connesso specificato, inclusi il nome, l'identità, le proprietà e altri dettagli del cluster.</span><span class="sxs-lookup"><span data-stu-id="a4fdd-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="a4fdd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4fdd-104">SYNTAX</span></span>

### <span data-ttu-id="a4fdd-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a4fdd-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a4fdd-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="a4fdd-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a4fdd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a4fdd-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4fdd-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="a4fdd-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a4fdd-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a4fdd-109">DESCRIPTION</span></span>
<span data-ttu-id="a4fdd-110">Restituisce le proprietà del cluster connesso specificato, inclusi il nome, l'identità, le proprietà e altri dettagli del cluster.</span><span class="sxs-lookup"><span data-stu-id="a4fdd-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="a4fdd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4fdd-111">EXAMPLES</span></span>

### <span data-ttu-id="a4fdd-112">Esempio 1: Ottieni tutti i kubernet connessi sotto un abbonamento</span><span class="sxs-lookup"><span data-stu-id="a4fdd-112">Example 1: Get all connected kubernetes under a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes

Location Name              Type
-------- ----              ----
eastus   connected-aks       Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks  Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks1 Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks3 Microsoft.Kubernetes/connectedClusters
eastus   connected-aks-cli1  Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="a4fdd-113">Questo comando consente di collegare tutti i kubernet connessi tramite un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a4fdd-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="a4fdd-114">Esempio 2: Ottenere tutti i kubernet connessi nel gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a4fdd-114">Example 2: Get all connected kubernetes under the resource group</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks

Location Name              Type
-------- ----              ----
eastus   connected-aks       Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks  Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks1 Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks3 Microsoft.Kubernetes/connectedClusters
eastus   connected-aks-cli1  Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="a4fdd-115">Questo comando consente di ottenere tutti i kubernet connessi nel gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a4fdd-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="a4fdd-116">Esempio 3: Creare un kubernet connesso</span><span class="sxs-lookup"><span data-stu-id="a4fdd-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="a4fdd-117">Questo comando ottiene un kubernet connesso.</span><span class="sxs-lookup"><span data-stu-id="a4fdd-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="a4fdd-118">Esempio 4: Ottenere un kubernet connesso per oggetto</span><span class="sxs-lookup"><span data-stu-id="a4fdd-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="a4fdd-119">Questo comando recupera un kubernet connesso dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a4fdd-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="a4fdd-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4fdd-120">PARAMETERS</span></span>

### <span data-ttu-id="a4fdd-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a4fdd-121">-ClusterName</span></span>
<span data-ttu-id="a4fdd-122">Il nome del cluster Kubernetes su cui si chiama get.</span><span class="sxs-lookup"><span data-stu-id="a4fdd-122">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4fdd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4fdd-123">-DefaultProfile</span></span>
<span data-ttu-id="a4fdd-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4fdd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4fdd-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4fdd-125">-InputObject</span></span>
<span data-ttu-id="a4fdd-126">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a4fdd-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4fdd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4fdd-127">-ResourceGroupName</span></span>
<span data-ttu-id="a4fdd-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a4fdd-128">The name of the resource group.</span></span>
<span data-ttu-id="a4fdd-129">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a4fdd-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4fdd-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4fdd-130">-SubscriptionId</span></span>
<span data-ttu-id="a4fdd-131">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a4fdd-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4fdd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4fdd-132">CommonParameters</span></span>
<span data-ttu-id="a4fdd-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4fdd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4fdd-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a4fdd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4fdd-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="a4fdd-135">INPUTS</span></span>

### <span data-ttu-id="a4fdd-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="a4fdd-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="a4fdd-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4fdd-137">OUTPUTS</span></span>

### <span data-ttu-id="a4fdd-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="a4fdd-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span></span>

## <span data-ttu-id="a4fdd-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="a4fdd-139">NOTES</span></span>

<span data-ttu-id="a4fdd-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a4fdd-140">ALIASES</span></span>

<span data-ttu-id="a4fdd-141">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="a4fdd-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a4fdd-142">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a4fdd-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a4fdd-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a4fdd-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a4fdd-144">INPUTOBJECT <IConnectedKubernetesIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="a4fdd-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a4fdd-145">`[ClusterName <String>]`: il nome del cluster Kubernetes su cui si chiama get.</span><span class="sxs-lookup"><span data-stu-id="a4fdd-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="a4fdd-146">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="a4fdd-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a4fdd-147">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a4fdd-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a4fdd-148">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a4fdd-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="a4fdd-149">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a4fdd-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="a4fdd-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4fdd-150">RELATED LINKS</span></span>

