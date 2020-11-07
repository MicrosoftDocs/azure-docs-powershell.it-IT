---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/new-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
ms.openlocfilehash: 76719250ca7909d86d288b987b9598a58ab5fb88
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684652"
---
# <span data-ttu-id="a6d1f-101">New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a6d1f-101">New-AzContainerGroup</span></span>

## <span data-ttu-id="a6d1f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6d1f-102">SYNOPSIS</span></span>
<span data-ttu-id="a6d1f-103">Crea un gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-103">Creates a container group.</span></span>

## <span data-ttu-id="a6d1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6d1f-104">SYNTAX</span></span>

### <span data-ttu-id="a6d1f-105">CreateContainerGroupBaseParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a6d1f-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-AssignIdentity] [-OsType <String>]
 [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6d1f-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="a6d1f-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-AssignIdentity] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6d1f-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span><span class="sxs-lookup"><span data-stu-id="a6d1f-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6d1f-108">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6d1f-108">ExplicitIdentityParameterSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6d1f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6d1f-109">DESCRIPTION</span></span>
<span data-ttu-id="a6d1f-110">Il cmdlet **New-AzContainerGroup** crea un gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-110">The **New-AzContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="a6d1f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6d1f-111">EXAMPLES</span></span>

### <span data-ttu-id="a6d1f-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a6d1f-112">Example 1</span></span>
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

<span data-ttu-id="a6d1f-113">Questo comando crea un gruppo di contenitori usando l'ultima immagine di nginx e richiede un indirizzo IP pubblico con la porta di apertura 8000.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-113">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="a6d1f-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a6d1f-114">Example 2</span></span>
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

<span data-ttu-id="a6d1f-115">Questo comando crea un gruppo di contenitori ed esegue uno script personalizzato all'interno del contenitore.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-115">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="a6d1f-116">Esempio 3: crea un gruppo di contenitori da eseguire a completamento.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-116">Example 3: Creates a run-to-completion container group.</span></span>
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

<span data-ttu-id="a6d1f-117">Questo comando crea un gruppo di contenitori che stampa "Hello" e si arresta.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-117">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="a6d1f-118">Esempio 4: crea un gruppo di contenitori usando Image in Azure container Registry</span><span class="sxs-lookup"><span data-stu-id="a6d1f-118">Example 4: Creates a container group using image in Azure Container Registry</span></span>
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

<span data-ttu-id="a6d1f-119">Questo comando crea un gruppo di contenitori usando un'immagine nginx in Azure container Registry.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-119">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="a6d1f-120">Esempio 5: crea un gruppo di contenitori usando l'immagine nel registro di sistema immagine contenitore personalizzato</span><span class="sxs-lookup"><span data-stu-id="a6d1f-120">Example 5: Creates a container group using image in custom container image registry</span></span>
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

<span data-ttu-id="a6d1f-121">Questo comando consente di creare un gruppo di contenitori usando un'immagine personalizzata da un registro delle immagini di un contenitore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-121">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="a6d1f-122">Esempio 6: crea un gruppo di contenitori che monta il volume di file di Azure</span><span class="sxs-lookup"><span data-stu-id="a6d1f-122">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image alpine -AzFileVolumeShareName myshare -AzFileVolumeAccountKey $mycred -AzFileVolumeMountPath /mnt/azfile

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

<span data-ttu-id="a6d1f-123">Questo comando crea un gruppo di contenitori che monta la condivisione di file Azure specificata `/mnt/azfile` .</span><span class="sxs-lookup"><span data-stu-id="a6d1f-123">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

### <span data-ttu-id="a6d1f-124">Esempio 7</span><span class="sxs-lookup"><span data-stu-id="a6d1f-124">Example 7</span></span>
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

<span data-ttu-id="a6d1f-125">Questo comando crea un gruppo di contenitori con identità assegnata al sistema usando l'ultima immagine di nginx e richiede un indirizzo IP pubblico con la porta di apertura 8000.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-125">This commands creates a container group with system assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="a6d1f-126">Esempio 8</span><span class="sxs-lookup"><span data-stu-id="a6d1f-126">Example 8</span></span>
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

<span data-ttu-id="a6d1f-127">Questo comando crea un gruppo di contenitori con il sistema assegnato e l'identità assegnata dall'utente usando l'ultima immagine di nginx e richiede un indirizzo IP pubblico con la porta di apertura 8000.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-127">This commands creates a container group with system assigned and user assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

## <span data-ttu-id="a6d1f-128">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6d1f-128">PARAMETERS</span></span>

### <span data-ttu-id="a6d1f-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a6d1f-129">-AssignIdentity</span></span>
<span data-ttu-id="a6d1f-130">Abilitare l'identità assegnata al sistema</span><span class="sxs-lookup"><span data-stu-id="a6d1f-130">Enable system assigned identity</span></span>

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

### <span data-ttu-id="a6d1f-131">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a6d1f-131">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="a6d1f-132">Le credenziali dell'account di archiviazione della condivisione file di Azure da montare in cui il nome utente è l'account di archiviazione e la chiave è la chiave dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-132">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

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

### <span data-ttu-id="a6d1f-133">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="a6d1f-133">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="a6d1f-134">Il percorso di montaggio per il volume del file Azure.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-134">The mount path for the Azure File volume.</span></span>

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

### <span data-ttu-id="a6d1f-135">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="a6d1f-135">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="a6d1f-136">Nome della condivisione di file di Azure da montare.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-136">The name of the Azure File share to mount.</span></span>

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

### <span data-ttu-id="a6d1f-137">-Comando</span><span class="sxs-lookup"><span data-stu-id="a6d1f-137">-Command</span></span>
<span data-ttu-id="a6d1f-138">Comando da eseguire nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-138">The command to run in the container.</span></span>

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

### <span data-ttu-id="a6d1f-139">-CPU</span><span class="sxs-lookup"><span data-stu-id="a6d1f-139">-Cpu</span></span>
<span data-ttu-id="a6d1f-140">I core CPU necessari.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-140">The required CPU cores.</span></span>
<span data-ttu-id="a6d1f-141">Impostazione predefinita: 1</span><span class="sxs-lookup"><span data-stu-id="a6d1f-141">Default: 1</span></span>

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

### <span data-ttu-id="a6d1f-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6d1f-142">-DefaultProfile</span></span>
<span data-ttu-id="a6d1f-143">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6d1f-144">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="a6d1f-144">-DnsNameLabel</span></span>
<span data-ttu-id="a6d1f-145">Etichetta nome DNS per l'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-145">The DNS name label for the IP address.</span></span>

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

### <span data-ttu-id="a6d1f-146">-Metodo EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="a6d1f-146">-EnvironmentVariable</span></span>
<span data-ttu-id="a6d1f-147">Variabili di ambiente contenitore.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-147">The container environment variables.</span></span>

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

### <span data-ttu-id="a6d1f-148">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="a6d1f-148">-IdentityId</span></span>
<span data-ttu-id="a6d1f-149">ID identità assegnati dall'utente</span><span class="sxs-lookup"><span data-stu-id="a6d1f-149">The user assigned identity IDs</span></span>

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

### <span data-ttu-id="a6d1f-150">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="a6d1f-150">-IdentityType</span></span>
<span data-ttu-id="a6d1f-151">Tipo di identità gestita</span><span class="sxs-lookup"><span data-stu-id="a6d1f-151">The managed identity type</span></span>

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

### <span data-ttu-id="a6d1f-152">-Immagine</span><span class="sxs-lookup"><span data-stu-id="a6d1f-152">-Image</span></span>
<span data-ttu-id="a6d1f-153">Immagine del contenitore.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-153">The container image.</span></span>

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

### <span data-ttu-id="a6d1f-154">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="a6d1f-154">-IpAddressType</span></span>
<span data-ttu-id="a6d1f-155">Tipo di indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-155">The IP address type.</span></span>

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

### <span data-ttu-id="a6d1f-156">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a6d1f-156">-Location</span></span>
<span data-ttu-id="a6d1f-157">Posizione del gruppo contenitore.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-157">The container group Location.</span></span>
<span data-ttu-id="a6d1f-158">Impostazione predefinita per la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-158">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="a6d1f-159">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="a6d1f-159">-MemoryInGB</span></span>
<span data-ttu-id="a6d1f-160">La memoria necessaria in GB.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-160">The required memory in GB.</span></span>
<span data-ttu-id="a6d1f-161">Impostazione predefinita: 1,5</span><span class="sxs-lookup"><span data-stu-id="a6d1f-161">Default: 1.5</span></span>

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

### <span data-ttu-id="a6d1f-162">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6d1f-162">-Name</span></span>
<span data-ttu-id="a6d1f-163">Nome del gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-163">The container group name.</span></span>

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

### <span data-ttu-id="a6d1f-164">-OsType</span><span class="sxs-lookup"><span data-stu-id="a6d1f-164">-OsType</span></span>
<span data-ttu-id="a6d1f-165">Tipo di sistema operativo contenitore.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-165">The container OS type.</span></span>
<span data-ttu-id="a6d1f-166">Impostazione predefinita: Linux</span><span class="sxs-lookup"><span data-stu-id="a6d1f-166">Default: Linux</span></span>

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

### <span data-ttu-id="a6d1f-167">-Porta</span><span class="sxs-lookup"><span data-stu-id="a6d1f-167">-Port</span></span>
<span data-ttu-id="a6d1f-168">Le porte da aprire.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-168">The port(s) to open.</span></span> <span data-ttu-id="a6d1f-169">Impostazione predefinita: [80]</span><span class="sxs-lookup"><span data-stu-id="a6d1f-169">Default: [80]</span></span>

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

### <span data-ttu-id="a6d1f-170">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="a6d1f-170">-RegistryCredential</span></span>
<span data-ttu-id="a6d1f-171">Credenziale del registro di sistema personalizzata.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-171">The custom container registry credential.</span></span>

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

### <span data-ttu-id="a6d1f-172">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="a6d1f-172">-RegistryServerDomain</span></span>
<span data-ttu-id="a6d1f-173">Server di accesso del registro di sistema personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-173">The custom container registry login server.</span></span>

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

### <span data-ttu-id="a6d1f-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6d1f-174">-ResourceGroupName</span></span>
<span data-ttu-id="a6d1f-175">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-175">The resource group name.</span></span>

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

### <span data-ttu-id="a6d1f-176">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="a6d1f-176">-RestartPolicy</span></span>
<span data-ttu-id="a6d1f-177">Criteri di riavvio del contenitore.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-177">The container restart policy.</span></span> <span data-ttu-id="a6d1f-178">Impostazione predefinita: sempre</span><span class="sxs-lookup"><span data-stu-id="a6d1f-178">Default: Always</span></span>

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

### <span data-ttu-id="a6d1f-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="a6d1f-179">-Tag</span></span>
<span data-ttu-id="a6d1f-180">{{Fill tag Description}}</span><span class="sxs-lookup"><span data-stu-id="a6d1f-180">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="a6d1f-181">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a6d1f-181">-Confirm</span></span>
<span data-ttu-id="a6d1f-182">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6d1f-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6d1f-183">-WhatIf</span></span>
<span data-ttu-id="a6d1f-184">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6d1f-185">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6d1f-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6d1f-186">CommonParameters</span></span>
<span data-ttu-id="a6d1f-187">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6d1f-188">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6d1f-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6d1f-189">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6d1f-189">INPUTS</span></span>

### <span data-ttu-id="a6d1f-190">System. String</span><span class="sxs-lookup"><span data-stu-id="a6d1f-190">System.String</span></span>

### <span data-ttu-id="a6d1f-191">System. String []</span><span class="sxs-lookup"><span data-stu-id="a6d1f-191">System.String[]</span></span>

### <span data-ttu-id="a6d1f-192">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a6d1f-192">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a6d1f-193">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6d1f-193">OUTPUTS</span></span>

### <span data-ttu-id="a6d1f-194">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a6d1f-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="a6d1f-195">Note</span><span class="sxs-lookup"><span data-stu-id="a6d1f-195">NOTES</span></span>

## <span data-ttu-id="a6d1f-196">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6d1f-196">RELATED LINKS</span></span>
