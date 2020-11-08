---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: c09c4b4c8d71d90bbbac0771c75ea3ea51ee05dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191149"
---
# <span data-ttu-id="76f65-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="76f65-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="76f65-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="76f65-102">SYNOPSIS</span></span>
<span data-ttu-id="76f65-103">Register-AzStackHCI crea una risorsa cloud Microsoft. AzureStackHCI che rappresenta il cluster locale e registra il cluster locale con Azure.</span><span class="sxs-lookup"><span data-stu-id="76f65-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="76f65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76f65-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="76f65-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76f65-105">DESCRIPTION</span></span>
<span data-ttu-id="76f65-106">Register-AzStackHCI crea una risorsa cloud Microsoft. AzureStackHCI che rappresenta il cluster locale e registra il cluster locale con Azure.</span><span class="sxs-lookup"><span data-stu-id="76f65-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="76f65-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76f65-107">EXAMPLES</span></span>

### <span data-ttu-id="76f65-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="76f65-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node.
```

<span data-ttu-id="76f65-109">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" result: Success ResourceId:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-RG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="76f65-109">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span></span>

### <span data-ttu-id="76f65-110">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="76f65-110">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="76f65-111">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-nomecomputer ClusterNode1 risultato: successo ResourceId:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-RG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="76f65-111">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1 Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="76f65-112">ESEMPIO 3</span><span class="sxs-lookup"><span data-stu-id="76f65-112">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="76f65-113">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -Region westus-resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG result: PendingForAdminConsent ResourceId:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="76f65-113">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="76f65-114">ESEMPIO 4</span><span class="sxs-lookup"><span data-stu-id="76f65-114">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="76f65-115">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-Region westus-resourceName HciCluster1-ID tenant "c31c0dbb-CE27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ere =-GraphAccessToken Acee.. rerrer-AccountId user1@corp1.com -EnvironmentName AzureCloud-nomecomputer node1hci-Credential Get-Credential result: Success ResourceId:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/Providers/Microsoft.AzureStackHCI/Clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="76f65-115">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

## <span data-ttu-id="76f65-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="76f65-116">PARAMETERS</span></span>

### <span data-ttu-id="76f65-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="76f65-117">-SubscriptionId</span></span>
<span data-ttu-id="76f65-118">Specifica l'abbonamento a Azure per creare la risorsa.</span><span class="sxs-lookup"><span data-stu-id="76f65-118">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="76f65-119">Questo è l'unico parametro obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="76f65-119">This is the only Mandatory parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f65-120">-Area geografica</span><span class="sxs-lookup"><span data-stu-id="76f65-120">-Region</span></span>
<span data-ttu-id="76f65-121">Specifica l'area geografica per creare la risorsa.</span><span class="sxs-lookup"><span data-stu-id="76f65-121">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="76f65-122">Il valore predefinito è Eastus.</span><span class="sxs-lookup"><span data-stu-id="76f65-122">Default is EastUS.</span></span>

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

### <span data-ttu-id="76f65-123">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="76f65-123">-ResourceName</span></span>
<span data-ttu-id="76f65-124">Specifica il nome della risorsa creata in Azure.</span><span class="sxs-lookup"><span data-stu-id="76f65-124">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="76f65-125">Se non specificato, viene usato il nome del cluster locale.</span><span class="sxs-lookup"><span data-stu-id="76f65-125">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="76f65-126">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="76f65-126">-TenantId</span></span>
<span data-ttu-id="76f65-127">Specifica Azure ID tenant.</span><span class="sxs-lookup"><span data-stu-id="76f65-127">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="76f65-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76f65-128">-ResourceGroupName</span></span>
<span data-ttu-id="76f65-129">Specifica il nome del gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="76f65-129">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="76f65-130">Se non specificato \<LocalClusterName\> -RG verrà usato come nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="76f65-130">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="76f65-131">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="76f65-131">-ArmAccessToken</span></span>
<span data-ttu-id="76f65-132">Specifica il token di accesso ARM.</span><span class="sxs-lookup"><span data-stu-id="76f65-132">Specifies the ARM access token.</span></span>
<span data-ttu-id="76f65-133">Specificando questo insieme a GraphAccessToken e AccountId si eviterà l'accesso interattivo di Azure.</span><span class="sxs-lookup"><span data-stu-id="76f65-133">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="76f65-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="76f65-134">-GraphAccessToken</span></span>
<span data-ttu-id="76f65-135">Specifica il token di accesso del grafico.</span><span class="sxs-lookup"><span data-stu-id="76f65-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="76f65-136">Specificando questo insieme a ArmAccessToken e AccountId si eviterà l'accesso interattivo di Azure.</span><span class="sxs-lookup"><span data-stu-id="76f65-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="76f65-137">-AccountId</span><span class="sxs-lookup"><span data-stu-id="76f65-137">-AccountId</span></span>
<span data-ttu-id="76f65-138">Specifica il token di accesso ARM.</span><span class="sxs-lookup"><span data-stu-id="76f65-138">Specifies the ARM access token.</span></span>
<span data-ttu-id="76f65-139">Specificando questo insieme a ArmAccessToken e GraphAccessToken si eviterà l'accesso interattivo di Azure.</span><span class="sxs-lookup"><span data-stu-id="76f65-139">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f65-140">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="76f65-140">-EnvironmentName</span></span>
<span data-ttu-id="76f65-141">Specifica l'ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="76f65-141">Specifies the Azure Environment.</span></span>
<span data-ttu-id="76f65-142">Il valore predefinito è AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="76f65-142">Default is AzureCloud.</span></span>
<span data-ttu-id="76f65-143">I valori validi sono AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="76f65-143">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f65-144">-Nomecomputer</span><span class="sxs-lookup"><span data-stu-id="76f65-144">-ComputerName</span></span>
<span data-ttu-id="76f65-145">Specifica il nome del cluster o uno del nodo del cluster nel cluster locale che viene registrato in Azure.</span><span class="sxs-lookup"><span data-stu-id="76f65-145">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f65-146">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="76f65-146">-Credential</span></span>
<span data-ttu-id="76f65-147">Specifica le credenziali per nomecomputer.</span><span class="sxs-lookup"><span data-stu-id="76f65-147">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="76f65-148">Il valore predefinito è l'esecuzione del cmdlet da parte dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="76f65-148">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f65-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f65-149">CommonParameters</span></span>
<span data-ttu-id="76f65-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76f65-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f65-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76f65-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f65-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="76f65-152">INPUTS</span></span>

## <span data-ttu-id="76f65-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76f65-153">OUTPUTS</span></span>

### <span data-ttu-id="76f65-154">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="76f65-154">PSCustomObject.</span></span> <span data-ttu-id="76f65-155">Restituisce le proprietà seguenti in PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="76f65-155">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="76f65-156">Risultato: successo o non riuscito o PendingForAdminConsent o annullato.</span><span class="sxs-lookup"><span data-stu-id="76f65-156">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="76f65-157">ResourceId: ID risorsa della risorsa creata in Azure.</span><span class="sxs-lookup"><span data-stu-id="76f65-157">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="76f65-158">PortalResourceURL: URL delle risorse di Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="76f65-158">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="76f65-159">PortalAADAppPermissionsURL: URL del portale di Azure per la pagina delle autorizzazioni dell'app AAD.</span><span class="sxs-lookup"><span data-stu-id="76f65-159">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="76f65-160">Note</span><span class="sxs-lookup"><span data-stu-id="76f65-160">NOTES</span></span>

## <span data-ttu-id="76f65-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76f65-161">RELATED LINKS</span></span>
