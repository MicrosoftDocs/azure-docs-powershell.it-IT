---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: ad9c09118252499f99708ae99d36ee9ba2418ff2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474848"
---
# <span data-ttu-id="f116e-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="f116e-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="f116e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f116e-102">SYNOPSIS</span></span>
<span data-ttu-id="f116e-103">Register-AzStackHCI crea una risorsa cloud Microsoft. AzureStackHCI che rappresenta il cluster locale e registra il cluster locale con Azure.</span><span class="sxs-lookup"><span data-stu-id="f116e-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="f116e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f116e-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-CertificateThumbprint] <String>] [-RepairRegistration]
 [-UseDeviceAuthentication] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="f116e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f116e-105">DESCRIPTION</span></span>
<span data-ttu-id="f116e-106">Register-AzStackHCI crea una risorsa cloud Microsoft. AzureStackHCI che rappresenta il cluster locale e registra il cluster locale con Azure.</span><span class="sxs-lookup"><span data-stu-id="f116e-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="f116e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f116e-107">EXAMPLES</span></span>

### <span data-ttu-id="f116e-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="f116e-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node.
```

<span data-ttu-id="f116e-109">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" result: Success ResourceId:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-RG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="f116e-109">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span></span>

### <span data-ttu-id="f116e-110">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="f116e-110">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="f116e-111">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-nomecomputer ClusterNode1 risultato: successo ResourceId:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-RG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="f116e-111">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1 Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="f116e-112">ESEMPIO 3</span><span class="sxs-lookup"><span data-stu-id="f116e-112">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="f116e-113">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -Region westus-resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG result: PendingForAdminConsent ResourceId:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="f116e-113">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="f116e-114">ESEMPIO 4</span><span class="sxs-lookup"><span data-stu-id="f116e-114">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="f116e-115">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-Region westus-resourceName HciCluster1-ID tenant "c31c0dbb-CE27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ere =-GraphAccessToken Acee.. rerrer-AccountId user1@corp1.com -EnvironmentName AzureCloud-nomecomputer node1hci-Credential Get-Credential result: Success ResourceId:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/Providers/Microsoft.AzureStackHCI/Clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="f116e-115">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

## <span data-ttu-id="f116e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f116e-116">PARAMETERS</span></span>

### <span data-ttu-id="f116e-117">-AccountId</span><span class="sxs-lookup"><span data-stu-id="f116e-117">-AccountId</span></span>
<span data-ttu-id="f116e-118">Specifica il token di accesso ARM.</span><span class="sxs-lookup"><span data-stu-id="f116e-118">Specifies the ARM access token.</span></span>
<span data-ttu-id="f116e-119">Specificando questo insieme a ArmAccessToken e GraphAccessToken si eviterà l'accesso interattivo di Azure.</span><span class="sxs-lookup"><span data-stu-id="f116e-119">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f116e-120">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="f116e-120">-ArmAccessToken</span></span>
<span data-ttu-id="f116e-121">Specifica il token di accesso ARM.</span><span class="sxs-lookup"><span data-stu-id="f116e-121">Specifies the ARM access token.</span></span>
<span data-ttu-id="f116e-122">Specificando questo insieme a GraphAccessToken e AccountId si eviterà l'accesso interattivo di Azure.</span><span class="sxs-lookup"><span data-stu-id="f116e-122">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f116e-123">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="f116e-123">-CertificateThumbprint</span></span>
<span data-ttu-id="f116e-124">Specifica l'identificazione personale del certificato disponibile in tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="f116e-124">Specifies the thumbprint of the certificate available on all the nodes.</span></span> <span data-ttu-id="f116e-125">L'utente è responsabile della gestione del certificato.</span><span class="sxs-lookup"><span data-stu-id="f116e-125">User is responsible for managing the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f116e-126">-Nomecomputer</span><span class="sxs-lookup"><span data-stu-id="f116e-126">-ComputerName</span></span>
<span data-ttu-id="f116e-127">Specifica il nome del cluster o uno del nodo del cluster nel cluster locale che viene registrato in Azure.</span><span class="sxs-lookup"><span data-stu-id="f116e-127">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f116e-128">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="f116e-128">-Credential</span></span>
<span data-ttu-id="f116e-129">Specifica le credenziali per nomecomputer.</span><span class="sxs-lookup"><span data-stu-id="f116e-129">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="f116e-130">Il valore predefinito è l'esecuzione del cmdlet da parte dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="f116e-130">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f116e-131">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="f116e-131">-EnvironmentName</span></span>
<span data-ttu-id="f116e-132">Specifica l'ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="f116e-132">Specifies the Azure Environment.</span></span>
<span data-ttu-id="f116e-133">Il valore predefinito è AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="f116e-133">Default is AzureCloud.</span></span>
<span data-ttu-id="f116e-134">I valori validi sono AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="f116e-134">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f116e-135">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="f116e-135">-GraphAccessToken</span></span>
<span data-ttu-id="f116e-136">Specifica il token di accesso del grafico.</span><span class="sxs-lookup"><span data-stu-id="f116e-136">Specifies the Graph access token.</span></span>
<span data-ttu-id="f116e-137">Specificando questo insieme a ArmAccessToken e AccountId si eviterà l'accesso interattivo di Azure.</span><span class="sxs-lookup"><span data-stu-id="f116e-137">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f116e-138">-Area geografica</span><span class="sxs-lookup"><span data-stu-id="f116e-138">-Region</span></span>
<span data-ttu-id="f116e-139">Specifica l'area geografica per creare la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f116e-139">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="f116e-140">Il valore predefinito è Eastus.</span><span class="sxs-lookup"><span data-stu-id="f116e-140">Default is EastUS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f116e-141">-RepairRegistration</span><span class="sxs-lookup"><span data-stu-id="f116e-141">-RepairRegistration</span></span>
<span data-ttu-id="f116e-142">Ripristinare la registrazione corrente di Azure stack HCI con il cloud.</span><span class="sxs-lookup"><span data-stu-id="f116e-142">Repair the current Azure Stack HCI registration with the cloud.</span></span> <span data-ttu-id="f116e-143">Questo cmdlet elimina i certificati locali nei nodi raggruppati e i certificati remoti nell'applicazione Azure AD nel cloud e genera nuovi certificati sostitutivi per entrambi.</span><span class="sxs-lookup"><span data-stu-id="f116e-143">This cmdlet deletes the local certificates on the clustered nodes and the remote certificates in the Azure AD application in the cloud and generates new replacement certificates for both.</span></span> <span data-ttu-id="f116e-144">Il gruppo di risorse, il nome della risorsa e altre scelte di registrazione vengono mantenuti.</span><span class="sxs-lookup"><span data-stu-id="f116e-144">The resource group, resource name, and other registration choices are preserved.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f116e-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f116e-145">-ResourceGroupName</span></span>
<span data-ttu-id="f116e-146">Specifica il nome del gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="f116e-146">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="f116e-147">Se non specificato \<LocalClusterName\> -RG verrà usato come nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f116e-147">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f116e-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f116e-148">-ResourceName</span></span>
<span data-ttu-id="f116e-149">Specifica il nome della risorsa creata in Azure.</span><span class="sxs-lookup"><span data-stu-id="f116e-149">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="f116e-150">Se non specificato, viene usato il nome del cluster locale.</span><span class="sxs-lookup"><span data-stu-id="f116e-150">If not specified, on-premise cluster name is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f116e-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f116e-151">-SubscriptionId</span></span>
<span data-ttu-id="f116e-152">Specifica l'abbonamento a Azure per creare la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f116e-152">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="f116e-153">Questo è l'unico parametro obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f116e-153">This is the only Mandatory parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f116e-154">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="f116e-154">-TenantId</span></span>
<span data-ttu-id="f116e-155">Specifica Azure ID tenant.</span><span class="sxs-lookup"><span data-stu-id="f116e-155">Specifies the Azure TenantId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f116e-156">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="f116e-156">-UseDeviceAuthentication</span></span>
<span data-ttu-id="f116e-157">Usare l'autenticazione del codice del dispositivo invece di un prompt del browser interattivo.</span><span class="sxs-lookup"><span data-stu-id="f116e-157">Use device code authentication instead of an interactive browser prompt.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f116e-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f116e-158">CommonParameters</span></span>
<span data-ttu-id="f116e-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f116e-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f116e-160">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f116e-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f116e-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f116e-161">INPUTS</span></span>

## <span data-ttu-id="f116e-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f116e-162">OUTPUTS</span></span>

### <span data-ttu-id="f116e-163">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="f116e-163">PSCustomObject.</span></span> <span data-ttu-id="f116e-164">Restituisce le proprietà seguenti in PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="f116e-164">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="f116e-165">Risultato: successo o non riuscito o PendingForAdminConsent o annullato.</span><span class="sxs-lookup"><span data-stu-id="f116e-165">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="f116e-166">ResourceId: ID risorsa della risorsa creata in Azure.</span><span class="sxs-lookup"><span data-stu-id="f116e-166">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="f116e-167">PortalResourceURL: URL delle risorse di Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="f116e-167">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="f116e-168">PortalAADAppPermissionsURL: URL del portale di Azure per la pagina delle autorizzazioni dell'app AAD.</span><span class="sxs-lookup"><span data-stu-id="f116e-168">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="f116e-169">Note</span><span class="sxs-lookup"><span data-stu-id="f116e-169">NOTES</span></span>

## <span data-ttu-id="f116e-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f116e-170">RELATED LINKS</span></span>
