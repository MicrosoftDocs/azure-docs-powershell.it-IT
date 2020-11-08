---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: cc887fb8e41fd9464914144e7cbed5a332948228
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191148"
---
# <span data-ttu-id="e9928-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="e9928-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="e9928-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e9928-102">SYNOPSIS</span></span>
<span data-ttu-id="e9928-103">Unregister-AzStackHCI Elimina la risorsa cloud Microsoft. AzureStackHCI che rappresenta il cluster locale e Annulla la registrazione del cluster locale con Azure.</span><span class="sxs-lookup"><span data-stu-id="e9928-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="e9928-104">Le informazioni registrate disponibili nel cluster vengono usate per annullare la registrazione del cluster se non vengono passati parametri.</span><span class="sxs-lookup"><span data-stu-id="e9928-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="e9928-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9928-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9928-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9928-106">DESCRIPTION</span></span>
<span data-ttu-id="e9928-107">Unregister-AzStackHCI Elimina la risorsa cloud Microsoft. AzureStackHCI che rappresenta il cluster locale e Annulla la registrazione del cluster locale con Azure.</span><span class="sxs-lookup"><span data-stu-id="e9928-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="e9928-108">Le informazioni registrate disponibili nel cluster vengono usate per annullare la registrazione del cluster se non vengono passati parametri.</span><span class="sxs-lookup"><span data-stu-id="e9928-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="e9928-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9928-109">EXAMPLES</span></span>

### <span data-ttu-id="e9928-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="e9928-110">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node
```

<span data-ttu-id="e9928-111">C:\PS \> Unregister-risultato AzStackHCI: successo</span><span class="sxs-lookup"><span data-stu-id="e9928-111">C:\PS\>Unregister-AzStackHCI Result: Success</span></span>

### <span data-ttu-id="e9928-112">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="e9928-112">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="e9928-113">C:\PS \> Unregister-AzStackHCI-nomecomputer ClusterNode1 risultato: successo</span><span class="sxs-lookup"><span data-stu-id="e9928-113">C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1 Result: Success</span></span>

### <span data-ttu-id="e9928-114">ESEMPIO 3</span><span class="sxs-lookup"><span data-stu-id="e9928-114">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="e9928-115">C:\PS \> Unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG-Confirm: $false result: Success</span><span class="sxs-lookup"><span data-stu-id="e9928-115">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False Result: Success</span></span>

### <span data-ttu-id="e9928-116">ESEMPIO 4</span><span class="sxs-lookup"><span data-stu-id="e9928-116">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="e9928-117">C:\PS \> Unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-resourceName HciCluster1-ID tenant "c31c0dbb-CE27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ere =-GraphAccessToken Acee.. rerrer-AccountId user1@corp1.com -EnvironmentName AzureCloud-nomecomputer node1hci-credenziali Get-Credential risultato: successo</span><span class="sxs-lookup"><span data-stu-id="e9928-117">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success</span></span>

## <span data-ttu-id="e9928-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e9928-118">PARAMETERS</span></span>

### <span data-ttu-id="e9928-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e9928-119">-SubscriptionId</span></span>
<span data-ttu-id="e9928-120">Specifica l'abbonamento a Azure per creare la risorsa</span><span class="sxs-lookup"><span data-stu-id="e9928-120">Specifies the Azure Subscription to create the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9928-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e9928-121">-ResourceName</span></span>
<span data-ttu-id="e9928-122">Specifica il nome della risorsa creata in Azure.</span><span class="sxs-lookup"><span data-stu-id="e9928-122">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="e9928-123">Se non specificato, viene usato il nome del cluster locale.</span><span class="sxs-lookup"><span data-stu-id="e9928-123">If not specified, on-premise cluster name is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9928-124">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="e9928-124">-TenantId</span></span>
<span data-ttu-id="e9928-125">Specifica Azure ID tenant.</span><span class="sxs-lookup"><span data-stu-id="e9928-125">Specifies the Azure TenantId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9928-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9928-126">-ResourceGroupName</span></span>
<span data-ttu-id="e9928-127">Specifica il nome del gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="e9928-127">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="e9928-128">Se non specificato \<LocalClusterName\> -RG verrà usato come nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e9928-128">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9928-129">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="e9928-129">-ArmAccessToken</span></span>
<span data-ttu-id="e9928-130">Specifica il token di accesso ARM.</span><span class="sxs-lookup"><span data-stu-id="e9928-130">Specifies the ARM access token.</span></span>
<span data-ttu-id="e9928-131">Specificando questo insieme a GraphAccessToken e AccountId si eviterà l'accesso interattivo di Azure.</span><span class="sxs-lookup"><span data-stu-id="e9928-131">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9928-132">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="e9928-132">-GraphAccessToken</span></span>
<span data-ttu-id="e9928-133">Specifica il token di accesso del grafico.</span><span class="sxs-lookup"><span data-stu-id="e9928-133">Specifies the Graph access token.</span></span>
<span data-ttu-id="e9928-134">Specificando questo insieme a ArmAccessToken e AccountId si eviterà l'accesso interattivo di Azure.</span><span class="sxs-lookup"><span data-stu-id="e9928-134">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9928-135">-AccountId</span><span class="sxs-lookup"><span data-stu-id="e9928-135">-AccountId</span></span>
<span data-ttu-id="e9928-136">Specifica il token di accesso ARM.</span><span class="sxs-lookup"><span data-stu-id="e9928-136">Specifies the ARM access token.</span></span>
<span data-ttu-id="e9928-137">Specificando questo insieme a ArmAccessToken e GraphAccessToken si eviterà l'accesso interattivo di Azure.</span><span class="sxs-lookup"><span data-stu-id="e9928-137">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9928-138">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="e9928-138">-EnvironmentName</span></span>
<span data-ttu-id="e9928-139">Specifica l'ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="e9928-139">Specifies the Azure Environment.</span></span>
<span data-ttu-id="e9928-140">Il valore predefinito è AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="e9928-140">Default is AzureCloud.</span></span>
<span data-ttu-id="e9928-141">I valori validi sono AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="e9928-141">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9928-142">-Nomecomputer</span><span class="sxs-lookup"><span data-stu-id="e9928-142">-ComputerName</span></span>
<span data-ttu-id="e9928-143">Specifica uno dei nodi del cluster nel cluster locale che viene registrato in Azure.</span><span class="sxs-lookup"><span data-stu-id="e9928-143">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9928-144">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="e9928-144">-Credential</span></span>
<span data-ttu-id="e9928-145">Specifica le credenziali per nomecomputer.</span><span class="sxs-lookup"><span data-stu-id="e9928-145">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="e9928-146">Il valore predefinito è l'esecuzione del cmdlet da parte dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="e9928-146">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9928-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9928-147">-WhatIf</span></span>
<span data-ttu-id="e9928-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e9928-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9928-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e9928-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9928-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e9928-150">-Confirm</span></span>
<span data-ttu-id="e9928-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9928-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9928-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9928-152">CommonParameters</span></span>
<span data-ttu-id="e9928-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9928-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9928-154">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9928-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9928-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e9928-155">INPUTS</span></span>

## <span data-ttu-id="e9928-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9928-156">OUTPUTS</span></span>

### <span data-ttu-id="e9928-157">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="e9928-157">PSCustomObject.</span></span> <span data-ttu-id="e9928-158">Restituisce le proprietà seguenti in PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="e9928-158">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="e9928-159">Risultato: successo o non riuscito o annullato.</span><span class="sxs-lookup"><span data-stu-id="e9928-159">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="e9928-160">Note</span><span class="sxs-lookup"><span data-stu-id="e9928-160">NOTES</span></span>

## <span data-ttu-id="e9928-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9928-161">RELATED LINKS</span></span>
