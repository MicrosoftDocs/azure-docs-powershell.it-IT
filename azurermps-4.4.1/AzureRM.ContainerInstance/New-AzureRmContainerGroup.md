---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
ms.openlocfilehash: 63c54c5f1bb17af82e353b70e757bf91b1208958
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520122"
---
# <span data-ttu-id="a6923-101">New-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a6923-101">New-AzureRmContainerGroup</span></span>

## <span data-ttu-id="a6923-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6923-102">SYNOPSIS</span></span>
<span data-ttu-id="a6923-103">Crea un gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="a6923-103">Creates a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6923-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6923-104">SYNTAX</span></span>

### <span data-ttu-id="a6923-105">CreateContainerGroupBaseParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a6923-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> -Image <String> [-Location <String>]
 [-OsType <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-Port <Int32>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6923-106">CreateContainerGroupWithRegistryParamSet</span><span class="sxs-lookup"><span data-stu-id="a6923-106">CreateContainerGroupWithRegistryParamSet</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> -Image <String> [-Location <String>]
 [-OsType <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-Port <Int32>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>]
 -RegistryCredential <PSCredential> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6923-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6923-107">DESCRIPTION</span></span>
<span data-ttu-id="a6923-108">Il cmdlet **New-AzureRmContainerGroup** crea un gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="a6923-108">The **New-AzureRmContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="a6923-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6923-109">EXAMPLES</span></span>

### <span data-ttu-id="a6923-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a6923-110">Example 1</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port 8000

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
```

<span data-ttu-id="a6923-111">Questo comando crea un gruppo di contenitori usando l'ultima immagine di nginx e richiede un indirizzo IP pubblico con la porta di apertura 8000.</span><span class="sxs-lookup"><span data-stu-id="a6923-111">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="a6923-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a6923-112">Example 2</span></span>
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
```

<span data-ttu-id="a6923-113">Questo comando crea un gruppo di contenitori ed esegue uno script personalizzato all'interno del contenitore.</span><span class="sxs-lookup"><span data-stu-id="a6923-113">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="a6923-114">Esempio 3: crea un gruppo di contenitori usando Image in Azure container Registry</span><span class="sxs-lookup"><span data-stu-id="a6923-114">Example 3: Creates a container group using image in Azure Container Registry</span></span>
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
```

<span data-ttu-id="a6923-115">Questo comando crea un gruppo di contenitori usando un'immagine nginx in Azure container Registry.</span><span class="sxs-lookup"><span data-stu-id="a6923-115">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="a6923-116">Esempio 4: crea un gruppo di contenitori usando l'immagine nel registro di sistema immagine contenitore personalizzato</span><span class="sxs-lookup"><span data-stu-id="a6923-116">Example 4: Creates a container group using image in custom container image registry</span></span>
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
```

<span data-ttu-id="a6923-117">Questo comando consente di creare un gruppo di contenitori usando un'immagine personalizzata da un registro delle immagini di un contenitore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a6923-117">This commands creates a container group using a custom image from a custom container image registry.</span></span>

## <span data-ttu-id="a6923-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6923-118">PARAMETERS</span></span>

### <span data-ttu-id="a6923-119">-Comando</span><span class="sxs-lookup"><span data-stu-id="a6923-119">-Command</span></span>
<span data-ttu-id="a6923-120">Comando da eseguire nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="a6923-120">The command to run in the container.</span></span>

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

### <span data-ttu-id="a6923-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a6923-121">-Confirm</span></span>
<span data-ttu-id="a6923-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6923-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6923-123">-CPU</span><span class="sxs-lookup"><span data-stu-id="a6923-123">-Cpu</span></span>
<span data-ttu-id="a6923-124">I core CPU necessari.</span><span class="sxs-lookup"><span data-stu-id="a6923-124">The required CPU cores.</span></span>
<span data-ttu-id="a6923-125">Impostazione predefinita: 1</span><span class="sxs-lookup"><span data-stu-id="a6923-125">Default: 1</span></span>

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

### <span data-ttu-id="a6923-126">-Metodo EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="a6923-126">-EnvironmentVariable</span></span>
<span data-ttu-id="a6923-127">Variabili di ambiente contenitore.</span><span class="sxs-lookup"><span data-stu-id="a6923-127">The container environment variables.</span></span>

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

### <span data-ttu-id="a6923-128">-Immagine</span><span class="sxs-lookup"><span data-stu-id="a6923-128">-Image</span></span>
<span data-ttu-id="a6923-129">Immagine del contenitore.</span><span class="sxs-lookup"><span data-stu-id="a6923-129">The container image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6923-130">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="a6923-130">-IpAddressType</span></span>
<span data-ttu-id="a6923-131">Tipo di indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="a6923-131">The IP address type.</span></span>

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

### <span data-ttu-id="a6923-132">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a6923-132">-Location</span></span>
<span data-ttu-id="a6923-133">Posizione del gruppo contenitore.</span><span class="sxs-lookup"><span data-stu-id="a6923-133">The container group Location.</span></span>
<span data-ttu-id="a6923-134">Impostazione predefinita per la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a6923-134">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="a6923-135">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="a6923-135">-MemoryInGB</span></span>
<span data-ttu-id="a6923-136">La memoria necessaria in GB.</span><span class="sxs-lookup"><span data-stu-id="a6923-136">The required memory in GB.</span></span>
<span data-ttu-id="a6923-137">Impostazione predefinita: 1,5</span><span class="sxs-lookup"><span data-stu-id="a6923-137">Default: 1.5</span></span>

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

### <span data-ttu-id="a6923-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6923-138">-Name</span></span>
<span data-ttu-id="a6923-139">Nome del gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="a6923-139">The container group name.</span></span>

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

### <span data-ttu-id="a6923-140">-OsType</span><span class="sxs-lookup"><span data-stu-id="a6923-140">-OsType</span></span>
<span data-ttu-id="a6923-141">Tipo di sistema operativo contenitore.</span><span class="sxs-lookup"><span data-stu-id="a6923-141">The container OS type.</span></span>
<span data-ttu-id="a6923-142">Impostazione predefinita: Linux</span><span class="sxs-lookup"><span data-stu-id="a6923-142">Default: Linux</span></span>

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

### <span data-ttu-id="a6923-143">-Porta</span><span class="sxs-lookup"><span data-stu-id="a6923-143">-Port</span></span>
<span data-ttu-id="a6923-144">La porta da aprire.</span><span class="sxs-lookup"><span data-stu-id="a6923-144">The port to open.</span></span>
<span data-ttu-id="a6923-145">Impostazione predefinita: 80</span><span class="sxs-lookup"><span data-stu-id="a6923-145">Default: 80</span></span>

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

### <span data-ttu-id="a6923-146">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="a6923-146">-RegistryCredential</span></span>
<span data-ttu-id="a6923-147">Credenziale del registro di sistema personalizzata.</span><span class="sxs-lookup"><span data-stu-id="a6923-147">The custom container registry credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithRegistryParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6923-148">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="a6923-148">-RegistryServerDomain</span></span>
<span data-ttu-id="a6923-149">Server di accesso del registro di sistema personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a6923-149">The custom container registry login server.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithRegistryParamSet
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6923-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6923-150">-ResourceGroupName</span></span>
<span data-ttu-id="a6923-151">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a6923-151">The resource group name.</span></span>

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

### <span data-ttu-id="a6923-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="a6923-152">-Tag</span></span>
<span data-ttu-id="a6923-153">{{Fill tag Description}}</span><span class="sxs-lookup"><span data-stu-id="a6923-153">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="a6923-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6923-154">-WhatIf</span></span>
<span data-ttu-id="a6923-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6923-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6923-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6923-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6923-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6923-157">-DefaultProfile</span></span>
<span data-ttu-id="a6923-158">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6923-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6923-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6923-159">CommonParameters</span></span>
<span data-ttu-id="a6923-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6923-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6923-161">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6923-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6923-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6923-162">INPUTS</span></span>

### <span data-ttu-id="a6923-163">System. String</span><span class="sxs-lookup"><span data-stu-id="a6923-163">System.String</span></span>
<span data-ttu-id="a6923-164">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a6923-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a6923-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6923-165">OUTPUTS</span></span>

### <span data-ttu-id="a6923-166">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a6923-166">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="a6923-167">Note</span><span class="sxs-lookup"><span data-stu-id="a6923-167">NOTES</span></span>

## <span data-ttu-id="a6923-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6923-168">RELATED LINKS</span></span>

