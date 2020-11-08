---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: 1df844fc9a040fe20b6fdcdaa6f5dccda191aba4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191354"
---
# <span data-ttu-id="9e1da-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="9e1da-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="9e1da-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e1da-102">SYNOPSIS</span></span>
<span data-ttu-id="9e1da-103">Restituisce le proprietà del cluster connesso specificato, inclusi nome, identità, proprietà e dettagli del cluster aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="9e1da-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="9e1da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e1da-104">SYNTAX</span></span>

### <span data-ttu-id="9e1da-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9e1da-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9e1da-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="9e1da-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9e1da-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9e1da-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e1da-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="9e1da-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9e1da-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e1da-109">DESCRIPTION</span></span>
<span data-ttu-id="9e1da-110">Restituisce le proprietà del cluster connesso specificato, inclusi nome, identità, proprietà e dettagli del cluster aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="9e1da-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="9e1da-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e1da-111">EXAMPLES</span></span>

### <span data-ttu-id="9e1da-112">Esempio 1: ottenere tutti i kubernetes connessi in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="9e1da-112">Example 1: Get all connected kubernetes under a subscription</span></span>
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

<span data-ttu-id="9e1da-113">Questo comando ottiene tutti i kubernetes connessi in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="9e1da-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="9e1da-114">Esempio 2: ottenere tutte le kubernetes connesse nel gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="9e1da-114">Example 2: Get all connected kubernetes under the resource group</span></span>
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

<span data-ttu-id="9e1da-115">Questo comando ottiene tutti i kubernetes connessi nel gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="9e1da-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="9e1da-116">Esempio 3: ottenere un kubernetes connesso</span><span class="sxs-lookup"><span data-stu-id="9e1da-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="9e1da-117">Questo comando ottiene un kubernetes connesso.</span><span class="sxs-lookup"><span data-stu-id="9e1da-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="9e1da-118">Esempio 4: ottenere un kubernetes connesso per oggetto</span><span class="sxs-lookup"><span data-stu-id="9e1da-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="9e1da-119">Questo comando consente di ottenere un oggetto kubernetes connesso.</span><span class="sxs-lookup"><span data-stu-id="9e1da-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="9e1da-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e1da-120">PARAMETERS</span></span>

### <span data-ttu-id="9e1da-121">-Clustername</span><span class="sxs-lookup"><span data-stu-id="9e1da-121">-ClusterName</span></span>
<span data-ttu-id="9e1da-122">Nome del cluster Kubernetes in cui viene chiamato Get.</span><span class="sxs-lookup"><span data-stu-id="9e1da-122">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="9e1da-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e1da-123">-DefaultProfile</span></span>
<span data-ttu-id="9e1da-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e1da-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e1da-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e1da-125">-InputObject</span></span>
<span data-ttu-id="9e1da-126">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="9e1da-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9e1da-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e1da-127">-ResourceGroupName</span></span>
<span data-ttu-id="9e1da-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9e1da-128">The name of the resource group.</span></span>
<span data-ttu-id="9e1da-129">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="9e1da-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9e1da-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e1da-130">-SubscriptionId</span></span>
<span data-ttu-id="9e1da-131">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9e1da-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9e1da-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e1da-132">CommonParameters</span></span>
<span data-ttu-id="9e1da-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e1da-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e1da-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e1da-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e1da-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e1da-135">INPUTS</span></span>

### <span data-ttu-id="9e1da-136">Microsoft. Azure. PowerShell. Cmdlets. ConnectedKubernetes. Models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="9e1da-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="9e1da-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e1da-137">OUTPUTS</span></span>

### <span data-ttu-id="9e1da-138">Microsoft. Azure. PowerShell. Cmdlets. ConnectedKubernetes. Models. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="9e1da-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="9e1da-139">Note</span><span class="sxs-lookup"><span data-stu-id="9e1da-139">NOTES</span></span>

<span data-ttu-id="9e1da-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9e1da-140">ALIASES</span></span>

<span data-ttu-id="9e1da-141">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e1da-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9e1da-142">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="9e1da-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9e1da-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9e1da-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9e1da-144">INPUTOBJECT <IConnectedKubernetesIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="9e1da-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9e1da-145">`[ClusterName <String>]`: Nome del cluster Kubernetes in cui viene chiamato Get.</span><span class="sxs-lookup"><span data-stu-id="9e1da-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="9e1da-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="9e1da-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9e1da-147">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9e1da-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9e1da-148">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="9e1da-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="9e1da-149">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9e1da-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="9e1da-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e1da-150">RELATED LINKS</span></span>
