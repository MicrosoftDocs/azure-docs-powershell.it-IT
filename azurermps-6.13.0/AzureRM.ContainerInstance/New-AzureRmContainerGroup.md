---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/new-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
ms.openlocfilehash: 1823759b72bdb3162164068732f3a8201fcfb589
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509259"
---
# <span data-ttu-id="73224-101">New-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="73224-101">New-AzureRmContainerGroup</span></span>

## <span data-ttu-id="73224-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="73224-102">SYNOPSIS</span></span>
<span data-ttu-id="73224-103">Crea un gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="73224-103">Creates a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73224-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73224-104">SYNTAX</span></span>

### <span data-ttu-id="73224-105">CreateContainerGroupBaseParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="73224-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73224-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="73224-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73224-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73224-107">DESCRIPTION</span></span>
<span data-ttu-id="73224-108">Il cmdlet **New-AzureRmContainerGroup** crea un gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="73224-108">The **New-AzureRmContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="73224-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73224-109">EXAMPLES</span></span>

### <span data-ttu-id="73224-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="73224-110">Example 1</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000)

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

<span data-ttu-id="73224-111">Questo comando crea un gruppo di contenitori usando l'ultima immagine di nginx e richiede un indirizzo IP pubblico con la porta di apertura 8000.</span><span class="sxs-lookup"><span data-stu-id="73224-111">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="73224-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="73224-112">Example 2</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

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

<span data-ttu-id="73224-113">Questo comando crea un gruppo di contenitori ed esegue uno script personalizzato all'interno del contenitore.</span><span class="sxs-lookup"><span data-stu-id="73224-113">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="73224-114">Esempio 3: crea un gruppo di contenitori da eseguire a completamento.</span><span class="sxs-lookup"><span data-stu-id="73224-114">Example 3: Creates a run-to-completion container group.</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "echo hello" -RestartPolicy Never

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

<span data-ttu-id="73224-115">Questo comando crea un gruppo di contenitori che stampa "Hello" e si arresta.</span><span class="sxs-lookup"><span data-stu-id="73224-115">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="73224-116">Esempio 4: crea un gruppo di contenitori usando Image in Azure container Registry</span><span class="sxs-lookup"><span data-stu-id="73224-116">Example 4: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

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

<span data-ttu-id="73224-117">Questo comando crea un gruppo di contenitori usando un'immagine nginx in Azure container Registry.</span><span class="sxs-lookup"><span data-stu-id="73224-117">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="73224-118">Esempio 5: crea un gruppo di contenitori usando l'immagine nel registro di sistema immagine contenitore personalizzato</span><span class="sxs-lookup"><span data-stu-id="73224-118">Example 5: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

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

<span data-ttu-id="73224-119">Questo comando consente di creare un gruppo di contenitori usando un'immagine personalizzata da un registro delle immagini di un contenitore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="73224-119">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="73224-120">Esempio 6: crea un gruppo di contenitori che monta il volume di file di Azure</span><span class="sxs-lookup"><span data-stu-id="73224-120">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image alpine -AzureFileVolumeShareName myshare -AzureFileVolumeAccountKey $mycred -AzureFileVolumeMountPath /mnt/azfile

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

<span data-ttu-id="73224-121">Questo comando crea un gruppo di contenitori che monta la condivisione di file Azure specificata `/mnt/azfile` .</span><span class="sxs-lookup"><span data-stu-id="73224-121">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

## <span data-ttu-id="73224-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="73224-122">PARAMETERS</span></span>

### <span data-ttu-id="73224-123">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="73224-123">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="73224-124">Le credenziali dell'account di archiviazione della condivisione file di Azure da montare in cui il nome utente è l'account di archiviazione e la chiave è la chiave dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="73224-124">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73224-125">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="73224-125">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="73224-126">Il percorso di montaggio per il volume del file Azure.</span><span class="sxs-lookup"><span data-stu-id="73224-126">The mount path for the Azure File volume.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73224-127">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="73224-127">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="73224-128">Nome della condivisione di file di Azure da montare.</span><span class="sxs-lookup"><span data-stu-id="73224-128">The name of the Azure File share to mount.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73224-129">-Comando</span><span class="sxs-lookup"><span data-stu-id="73224-129">-Command</span></span>
<span data-ttu-id="73224-130">Comando da eseguire nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="73224-130">The command to run in the container.</span></span>

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

### <span data-ttu-id="73224-131">-CPU</span><span class="sxs-lookup"><span data-stu-id="73224-131">-Cpu</span></span>
<span data-ttu-id="73224-132">I core CPU necessari.</span><span class="sxs-lookup"><span data-stu-id="73224-132">The required CPU cores.</span></span>
<span data-ttu-id="73224-133">Impostazione predefinita: 1</span><span class="sxs-lookup"><span data-stu-id="73224-133">Default: 1</span></span>

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

### <span data-ttu-id="73224-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73224-134">-DefaultProfile</span></span>
<span data-ttu-id="73224-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="73224-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73224-136">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="73224-136">-DnsNameLabel</span></span>
<span data-ttu-id="73224-137">Etichetta nome DNS per l'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="73224-137">The DNS name label for the IP address.</span></span>

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

### <span data-ttu-id="73224-138">-Metodo EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="73224-138">-EnvironmentVariable</span></span>
<span data-ttu-id="73224-139">Variabili di ambiente contenitore.</span><span class="sxs-lookup"><span data-stu-id="73224-139">The container environment variables.</span></span>

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

### <span data-ttu-id="73224-140">-Immagine</span><span class="sxs-lookup"><span data-stu-id="73224-140">-Image</span></span>
<span data-ttu-id="73224-141">Immagine del contenitore.</span><span class="sxs-lookup"><span data-stu-id="73224-141">The container image.</span></span>

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

### <span data-ttu-id="73224-142">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="73224-142">-IpAddressType</span></span>
<span data-ttu-id="73224-143">Tipo di indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="73224-143">The IP address type.</span></span>

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

### <span data-ttu-id="73224-144">-Posizione</span><span class="sxs-lookup"><span data-stu-id="73224-144">-Location</span></span>
<span data-ttu-id="73224-145">Posizione del gruppo contenitore.</span><span class="sxs-lookup"><span data-stu-id="73224-145">The container group Location.</span></span>
<span data-ttu-id="73224-146">Impostazione predefinita per la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="73224-146">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="73224-147">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="73224-147">-MemoryInGB</span></span>
<span data-ttu-id="73224-148">La memoria necessaria in GB.</span><span class="sxs-lookup"><span data-stu-id="73224-148">The required memory in GB.</span></span>
<span data-ttu-id="73224-149">Impostazione predefinita: 1,5</span><span class="sxs-lookup"><span data-stu-id="73224-149">Default: 1.5</span></span>

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

### <span data-ttu-id="73224-150">-Nome</span><span class="sxs-lookup"><span data-stu-id="73224-150">-Name</span></span>
<span data-ttu-id="73224-151">Nome del gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="73224-151">The container group name.</span></span>

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

### <span data-ttu-id="73224-152">-OsType</span><span class="sxs-lookup"><span data-stu-id="73224-152">-OsType</span></span>
<span data-ttu-id="73224-153">Tipo di sistema operativo contenitore.</span><span class="sxs-lookup"><span data-stu-id="73224-153">The container OS type.</span></span>
<span data-ttu-id="73224-154">Impostazione predefinita: Linux</span><span class="sxs-lookup"><span data-stu-id="73224-154">Default: Linux</span></span>

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

### <span data-ttu-id="73224-155">-Porta</span><span class="sxs-lookup"><span data-stu-id="73224-155">-Port</span></span>
<span data-ttu-id="73224-156">Le porte da aprire.</span><span class="sxs-lookup"><span data-stu-id="73224-156">The port(s) to open.</span></span> <span data-ttu-id="73224-157">Impostazione predefinita: [80]</span><span class="sxs-lookup"><span data-stu-id="73224-157">Default: [80]</span></span>

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

### <span data-ttu-id="73224-158">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="73224-158">-RegistryCredential</span></span>
<span data-ttu-id="73224-159">Credenziale del registro di sistema personalizzata.</span><span class="sxs-lookup"><span data-stu-id="73224-159">The custom container registry credential.</span></span>

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

### <span data-ttu-id="73224-160">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="73224-160">-RegistryServerDomain</span></span>
<span data-ttu-id="73224-161">Server di accesso del registro di sistema personalizzato.</span><span class="sxs-lookup"><span data-stu-id="73224-161">The custom container registry login server.</span></span>

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

### <span data-ttu-id="73224-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73224-162">-ResourceGroupName</span></span>
<span data-ttu-id="73224-163">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="73224-163">The resource group name.</span></span>

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

### <span data-ttu-id="73224-164">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="73224-164">-RestartPolicy</span></span>
<span data-ttu-id="73224-165">Criteri di riavvio del contenitore.</span><span class="sxs-lookup"><span data-stu-id="73224-165">The container restart policy.</span></span> <span data-ttu-id="73224-166">Impostazione predefinita: sempre</span><span class="sxs-lookup"><span data-stu-id="73224-166">Default: Always</span></span>

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

### <span data-ttu-id="73224-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="73224-167">-Tag</span></span>
<span data-ttu-id="73224-168">{{Fill tag Description}}</span><span class="sxs-lookup"><span data-stu-id="73224-168">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="73224-169">-Confermare</span><span class="sxs-lookup"><span data-stu-id="73224-169">-Confirm</span></span>
<span data-ttu-id="73224-170">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73224-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73224-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73224-171">-WhatIf</span></span>
<span data-ttu-id="73224-172">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="73224-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73224-173">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="73224-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73224-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73224-174">CommonParameters</span></span>
<span data-ttu-id="73224-175">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73224-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73224-176">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73224-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73224-177">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="73224-177">INPUTS</span></span>

### <span data-ttu-id="73224-178">System. String</span><span class="sxs-lookup"><span data-stu-id="73224-178">System.String</span></span>

### <span data-ttu-id="73224-179">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="73224-179">System.Collections.Hashtable</span></span>

## <span data-ttu-id="73224-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73224-180">OUTPUTS</span></span>

### <span data-ttu-id="73224-181">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="73224-181">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="73224-182">Note</span><span class="sxs-lookup"><span data-stu-id="73224-182">NOTES</span></span>

## <span data-ttu-id="73224-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73224-183">RELATED LINKS</span></span>