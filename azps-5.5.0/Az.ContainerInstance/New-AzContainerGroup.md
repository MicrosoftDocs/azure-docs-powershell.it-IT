---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/new-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
ms.openlocfilehash: 20daa8d14f77ca4563c072d58d1c2269235cb164
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181503"
---
# <span data-ttu-id="17a00-101">New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="17a00-101">New-AzContainerGroup</span></span>

## <span data-ttu-id="17a00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17a00-102">SYNOPSIS</span></span>
<span data-ttu-id="17a00-103">Crea un gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="17a00-103">Creates a container group.</span></span>

## <span data-ttu-id="17a00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17a00-104">SYNTAX</span></span>

### <span data-ttu-id="17a00-105">CreateContainerGroupBaseParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="17a00-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-AssignIdentity] [-OsType <String>]
 [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17a00-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="17a00-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-AssignIdentity] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17a00-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span><span class="sxs-lookup"><span data-stu-id="17a00-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17a00-108">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="17a00-108">ExplicitIdentityParameterSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17a00-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="17a00-109">DESCRIPTION</span></span>
<span data-ttu-id="17a00-110">I cmdlet **New-AzContainerGroup** creano un gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="17a00-110">The **New-AzContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="17a00-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17a00-111">EXAMPLES</span></span>

### <span data-ttu-id="17a00-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="17a00-112">Example 1</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000)

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="17a00-113">Questo comando crea un gruppo di contenitori con l'immagine nginx più recente e richiede un indirizzo IP pubblico con la porta 8000 aperta.</span><span class="sxs-lookup"><span data-stu-id="17a00-113">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="17a00-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="17a00-114">Example 2</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="17a00-115">Questo comando crea un gruppo di contenitori ed esegue uno script personalizzato all'interno del contenitore.</span><span class="sxs-lookup"><span data-stu-id="17a00-115">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="17a00-116">Esempio 3: Crea un gruppo di contenitori da eseguire a completamento.</span><span class="sxs-lookup"><span data-stu-id="17a00-116">Example 3: Creates a run-to-completion container group.</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "echo hello" -RestartPolicy Never

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="17a00-117">Questo comando crea un gruppo di contenitori che stampa "ciao" e si ferma.</span><span class="sxs-lookup"><span data-stu-id="17a00-117">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="17a00-118">Esempio 4: Crea un gruppo di contenitori usando un'immagine nel Registro di sistema di Contenitori di Azure</span><span class="sxs-lookup"><span data-stu-id="17a00-118">Example 4: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myacr}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="17a00-119">Questo comando crea un gruppo di contenitori con un'immagine nginx nel Registro di sistema di Azure Container.</span><span class="sxs-lookup"><span data-stu-id="17a00-119">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="17a00-120">Esempio 5: Crea un gruppo di contenitori usando un'immagine nel Registro di sistema delle immagini del contenitore personalizzato</span><span class="sxs-lookup"><span data-stu-id="17a00-120">Example 5: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="17a00-121">Questo comando crea un gruppo di contenitori usando un'immagine personalizzata da un registro immagini contenitore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="17a00-121">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="17a00-122">Esempio 6: Crea un gruppo di contenitori che monta il volume dei file di Azure</span><span class="sxs-lookup"><span data-stu-id="17a00-122">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name mycontainer -Image alpine -AzureFileVolumeShareName myshare -AzureFileVolumeAccountCredential $mycred -AzureFileVolumeMountPath /mnt/azfile

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  : {AzureFile}
State                    : Running
Events                   : {}
```

<span data-ttu-id="17a00-123">Questo comando crea un gruppo di contenitori in cui viene montata la condivisione file di Azure `/mnt/azfile` specificata.</span><span class="sxs-lookup"><span data-stu-id="17a00-123">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

### <span data-ttu-id="17a00-124">Esempio 7</span><span class="sxs-lookup"><span data-stu-id="17a00-124">Example 7</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -AssignIdentity

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="17a00-125">Questo comando crea un gruppo di contenitori con l'identità assegnata al sistema usando l'immagine nginx più recente e richiede un indirizzo IP pubblico con la porta 8000 aperta.</span><span class="sxs-lookup"><span data-stu-id="17a00-125">This commands creates a container group with system assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="17a00-126">Esempio 8</span><span class="sxs-lookup"><span data-stu-id="17a00-126">Example 8</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -IdentityType SystemAssignedUserAssigned -IdentityId /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<UserIdentityName>

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="17a00-127">Questo comando crea un gruppo di contenitori con il sistema assegnato e l'identità assegnata all'utente usando l'immagine nginx più recente e richiede un indirizzo IP pubblico con la porta 8000 di apertura.</span><span class="sxs-lookup"><span data-stu-id="17a00-127">This commands creates a container group with system assigned and user assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

## <span data-ttu-id="17a00-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17a00-128">PARAMETERS</span></span>

### <span data-ttu-id="17a00-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="17a00-129">-AssignIdentity</span></span>
<span data-ttu-id="17a00-130">Abilitare l'identità assegnata al sistema</span><span class="sxs-lookup"><span data-stu-id="17a00-130">Enable system assigned identity</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateContainerGroupBaseParamSet, CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a00-131">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="17a00-131">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="17a00-132">Credenziali dell'account di archiviazione della condivisione file di Azure da installare, dove il nome utente è il nome dell'account di archiviazione e la chiave è la chiave dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="17a00-132">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a00-133">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="17a00-133">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="17a00-134">Percorso di montaggio per il volume File di Azure.</span><span class="sxs-lookup"><span data-stu-id="17a00-134">The mount path for the Azure File volume.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a00-135">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="17a00-135">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="17a00-136">Nome della condivisione file di Azure da montare.</span><span class="sxs-lookup"><span data-stu-id="17a00-136">The name of the Azure File share to mount.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a00-137">-Command</span><span class="sxs-lookup"><span data-stu-id="17a00-137">-Command</span></span>
<span data-ttu-id="17a00-138">Comando da eseguire nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="17a00-138">The command to run in the container.</span></span>

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

### <span data-ttu-id="17a00-139">-Cpu</span><span class="sxs-lookup"><span data-stu-id="17a00-139">-Cpu</span></span>
<span data-ttu-id="17a00-140">Core della CPU necessari.</span><span class="sxs-lookup"><span data-stu-id="17a00-140">The required CPU cores.</span></span>
<span data-ttu-id="17a00-141">Impostazione predefinita: 1</span><span class="sxs-lookup"><span data-stu-id="17a00-141">Default: 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a00-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17a00-142">-DefaultProfile</span></span>
<span data-ttu-id="17a00-143">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="17a00-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17a00-144">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="17a00-144">-DnsNameLabel</span></span>
<span data-ttu-id="17a00-145">Etichetta del nome DNS per l'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="17a00-145">The DNS name label for the IP address.</span></span>

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

### <span data-ttu-id="17a00-146">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="17a00-146">-EnvironmentVariable</span></span>
<span data-ttu-id="17a00-147">Variabili dell'ambiente contenitore.</span><span class="sxs-lookup"><span data-stu-id="17a00-147">The container environment variables.</span></span>

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

### <span data-ttu-id="17a00-148">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="17a00-148">-IdentityId</span></span>
<span data-ttu-id="17a00-149">ID identità assegnati dall'utente</span><span class="sxs-lookup"><span data-stu-id="17a00-149">The user assigned identity IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17a00-150">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="17a00-150">-IdentityType</span></span>
<span data-ttu-id="17a00-151">Tipo di identità gestita</span><span class="sxs-lookup"><span data-stu-id="17a00-151">The managed identity type</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerInstance.Models.ResourceIdentityType
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet, ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a00-152">-Image</span><span class="sxs-lookup"><span data-stu-id="17a00-152">-Image</span></span>
<span data-ttu-id="17a00-153">Immagine del contenitore.</span><span class="sxs-lookup"><span data-stu-id="17a00-153">The container image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a00-154">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="17a00-154">-IpAddressType</span></span>
<span data-ttu-id="17a00-155">Il tipo di indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="17a00-155">The IP address type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Public

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a00-156">-Location</span><span class="sxs-lookup"><span data-stu-id="17a00-156">-Location</span></span>
<span data-ttu-id="17a00-157">Posizione del gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="17a00-157">The container group Location.</span></span>
<span data-ttu-id="17a00-158">Impostazione predefinita per il percorso del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="17a00-158">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="17a00-159">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="17a00-159">-MemoryInGB</span></span>
<span data-ttu-id="17a00-160">La memoria richiesta in GB.</span><span class="sxs-lookup"><span data-stu-id="17a00-160">The required memory in GB.</span></span>
<span data-ttu-id="17a00-161">Impostazione predefinita: 1,5</span><span class="sxs-lookup"><span data-stu-id="17a00-161">Default: 1.5</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases: Memory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a00-162">-Name</span><span class="sxs-lookup"><span data-stu-id="17a00-162">-Name</span></span>
<span data-ttu-id="17a00-163">Nome del gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="17a00-163">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17a00-164">-OsType</span><span class="sxs-lookup"><span data-stu-id="17a00-164">-OsType</span></span>
<span data-ttu-id="17a00-165">Il tipo di sistema operativo contenitore.</span><span class="sxs-lookup"><span data-stu-id="17a00-165">The container OS type.</span></span>
<span data-ttu-id="17a00-166">Impostazione predefinita: Linux</span><span class="sxs-lookup"><span data-stu-id="17a00-166">Default: Linux</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Linux, Windows

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a00-167">-Porta</span><span class="sxs-lookup"><span data-stu-id="17a00-167">-Port</span></span>
<span data-ttu-id="17a00-168">Le porte da aprire.</span><span class="sxs-lookup"><span data-stu-id="17a00-168">The port(s) to open.</span></span> <span data-ttu-id="17a00-169">Impostazione predefinita: [80]</span><span class="sxs-lookup"><span data-stu-id="17a00-169">Default: [80]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a00-170">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="17a00-170">-RegistryCredential</span></span>
<span data-ttu-id="17a00-171">Credenziali del Registro di sistema del contenitore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="17a00-171">The custom container registry credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a00-172">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="17a00-172">-RegistryServerDomain</span></span>
<span data-ttu-id="17a00-173">Server di accesso al Registro di sistema del contenitore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="17a00-173">The custom container registry login server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a00-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17a00-174">-ResourceGroupName</span></span>
<span data-ttu-id="17a00-175">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="17a00-175">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17a00-176">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="17a00-176">-RestartPolicy</span></span>
<span data-ttu-id="17a00-177">Criterio di riavvio del contenitore.</span><span class="sxs-lookup"><span data-stu-id="17a00-177">The container restart policy.</span></span> <span data-ttu-id="17a00-178">Impostazione predefinita: Sempre</span><span class="sxs-lookup"><span data-stu-id="17a00-178">Default: Always</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Always, Never, OnFailure

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a00-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="17a00-179">-Tag</span></span>
<span data-ttu-id="17a00-180">{{Fill Tag Description}}</span><span class="sxs-lookup"><span data-stu-id="17a00-180">{{Fill Tag Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17a00-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17a00-181">-Confirm</span></span>
<span data-ttu-id="17a00-182">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17a00-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17a00-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17a00-183">-WhatIf</span></span>
<span data-ttu-id="17a00-184">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17a00-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17a00-185">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17a00-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17a00-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17a00-186">CommonParameters</span></span>
<span data-ttu-id="17a00-187">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17a00-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17a00-188">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17a00-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17a00-189">INPUT</span><span class="sxs-lookup"><span data-stu-id="17a00-189">INPUTS</span></span>

### <span data-ttu-id="17a00-190">System.String</span><span class="sxs-lookup"><span data-stu-id="17a00-190">System.String</span></span>

### <span data-ttu-id="17a00-191">System.String[]</span><span class="sxs-lookup"><span data-stu-id="17a00-191">System.String[]</span></span>

### <span data-ttu-id="17a00-192">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="17a00-192">System.Collections.Hashtable</span></span>

## <span data-ttu-id="17a00-193">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17a00-193">OUTPUTS</span></span>

### <span data-ttu-id="17a00-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="17a00-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="17a00-195">NOTE</span><span class="sxs-lookup"><span data-stu-id="17a00-195">NOTES</span></span>

## <span data-ttu-id="17a00-196">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17a00-196">RELATED LINKS</span></span>
