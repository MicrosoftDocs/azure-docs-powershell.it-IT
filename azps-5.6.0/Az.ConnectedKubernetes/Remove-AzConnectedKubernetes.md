---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 7abbe244e702c80f18d2c9e97236f74d60f094bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012478"
---
# <span data-ttu-id="608ea-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="608ea-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="608ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="608ea-102">SYNOPSIS</span></span>
<span data-ttu-id="608ea-103">Eliminare un cluster connesso, rimuovendo la risorsa monitorata in Gestione risorse di Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="608ea-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="608ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="608ea-104">SYNTAX</span></span>

### <span data-ttu-id="608ea-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="608ea-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="608ea-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="608ea-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="608ea-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="608ea-107">DESCRIPTION</span></span>
<span data-ttu-id="608ea-108">Eliminare un cluster connesso, rimuovendo la risorsa monitorata in Gestione risorse di Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="608ea-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="608ea-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="608ea-109">EXAMPLES</span></span>

### <span data-ttu-id="608ea-110">Esempio 1: Rimuovere un kubernet connesso</span><span class="sxs-lookup"><span data-stu-id="608ea-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="608ea-111">Questo comando rimuove un kubernet connesso</span><span class="sxs-lookup"><span data-stu-id="608ea-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="608ea-112">Esempio 2: Rimuovere un kubernet connesso dall'oggetto</span><span class="sxs-lookup"><span data-stu-id="608ea-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="608ea-113">Questo comando rimuove un kubernet connesso dall'oggetto</span><span class="sxs-lookup"><span data-stu-id="608ea-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="608ea-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="608ea-114">PARAMETERS</span></span>

### <span data-ttu-id="608ea-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="608ea-115">-AsJob</span></span>
<span data-ttu-id="608ea-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="608ea-116">Run the command as a job</span></span>

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

### <span data-ttu-id="608ea-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="608ea-117">-ClusterName</span></span>
<span data-ttu-id="608ea-118">Il nome del cluster Kubernetes su cui si chiama get.</span><span class="sxs-lookup"><span data-stu-id="608ea-118">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="608ea-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="608ea-119">-DefaultProfile</span></span>
<span data-ttu-id="608ea-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="608ea-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="608ea-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="608ea-121">-InputObject</span></span>
<span data-ttu-id="608ea-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="608ea-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="608ea-123">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="608ea-123">-KubeConfig</span></span>
<span data-ttu-id="608ea-124">Percorso del file di configurazione del kube</span><span class="sxs-lookup"><span data-stu-id="608ea-124">Path to the kube config file</span></span>

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

### <span data-ttu-id="608ea-125">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="608ea-125">-KubeContext</span></span>
<span data-ttu-id="608ea-126">Contesto Kubconfig dal computer corrente</span><span class="sxs-lookup"><span data-stu-id="608ea-126">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="608ea-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="608ea-127">-NoWait</span></span>
<span data-ttu-id="608ea-128">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="608ea-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="608ea-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="608ea-129">-PassThru</span></span>
<span data-ttu-id="608ea-130">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="608ea-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="608ea-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="608ea-131">-ResourceGroupName</span></span>
<span data-ttu-id="608ea-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="608ea-132">The name of the resource group.</span></span>
<span data-ttu-id="608ea-133">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="608ea-133">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="608ea-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="608ea-134">-SubscriptionId</span></span>
<span data-ttu-id="608ea-135">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="608ea-135">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="608ea-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="608ea-136">-Confirm</span></span>
<span data-ttu-id="608ea-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="608ea-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="608ea-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="608ea-138">-WhatIf</span></span>
<span data-ttu-id="608ea-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="608ea-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="608ea-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="608ea-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="608ea-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="608ea-141">CommonParameters</span></span>
<span data-ttu-id="608ea-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="608ea-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="608ea-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="608ea-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="608ea-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="608ea-144">INPUTS</span></span>

### <span data-ttu-id="608ea-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="608ea-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="608ea-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="608ea-146">OUTPUTS</span></span>

### <span data-ttu-id="608ea-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="608ea-147">System.Boolean</span></span>

## <span data-ttu-id="608ea-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="608ea-148">NOTES</span></span>

<span data-ttu-id="608ea-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="608ea-149">ALIASES</span></span>

<span data-ttu-id="608ea-150">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="608ea-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="608ea-151">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="608ea-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="608ea-152">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="608ea-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="608ea-153">INPUTOBJECT <IConnectedKubernetesIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="608ea-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="608ea-154">`[ClusterName <String>]`: il nome del cluster Kubernetes su cui si chiama get.</span><span class="sxs-lookup"><span data-stu-id="608ea-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="608ea-155">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="608ea-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="608ea-156">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="608ea-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="608ea-157">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="608ea-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="608ea-158">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="608ea-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="608ea-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="608ea-159">RELATED LINKS</span></span>

