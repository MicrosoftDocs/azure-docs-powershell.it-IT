---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: 242060652ea84d7fd85bc0907379ccb5b6eba478
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675069"
---
# <span data-ttu-id="1e9d3-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1e9d3-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="1e9d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1e9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="1e9d3-103">Aggiorna un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-103">Updates a container registry.</span></span>

## <span data-ttu-id="1e9d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e9d3-104">SYNTAX</span></span>

### <span data-ttu-id="1e9d3-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e9d3-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e9d3-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e9d3-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e9d3-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e9d3-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e9d3-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e9d3-111">DESCRIPTION</span></span>
<span data-ttu-id="1e9d3-112">Il cmdlet Update-AzContainerRegistry aggiorna un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="1e9d3-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e9d3-113">EXAMPLES</span></span>

### <span data-ttu-id="1e9d3-114">Esempio 1: abilitare l'utente dell'amministratore per un registro contenitore specificato</span><span class="sxs-lookup"><span data-stu-id="1e9d3-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="1e9d3-115">Questo comando consente all'utente di amministratore per il registro di sistema contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="1e9d3-116">Esempio 2: impostare l'account di archiviazione usato da un registro dei contenitori specificato</span><span class="sxs-lookup"><span data-stu-id="1e9d3-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="1e9d3-117">Questo comando imposta il registro di sistema del contenitore specificato per l'uso di un account di archiviazione esistente \` mystorageaccount \` nella stessa sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="1e9d3-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1e9d3-118">PARAMETERS</span></span>

### <span data-ttu-id="1e9d3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e9d3-119">-DefaultProfile</span></span>
<span data-ttu-id="1e9d3-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1e9d3-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e9d3-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="1e9d3-121">-DisableAdminUser</span></span>
<span data-ttu-id="1e9d3-122">Abilitare l'utente amministratore per il registro dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-122">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e9d3-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="1e9d3-123">-EnableAdminUser</span></span>
<span data-ttu-id="1e9d3-124">Abilitare l'utente amministratore per il registro dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-124">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e9d3-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e9d3-125">-Name</span></span>
<span data-ttu-id="1e9d3-126">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-126">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e9d3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e9d3-127">-ResourceGroupName</span></span>
<span data-ttu-id="1e9d3-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-128">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e9d3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e9d3-129">-ResourceId</span></span>
<span data-ttu-id="1e9d3-130">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="1e9d3-130">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e9d3-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="1e9d3-131">-Sku</span></span>
<span data-ttu-id="1e9d3-132">SKU del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-132">Container Registry SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e9d3-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1e9d3-133">-StorageAccountName</span></span>
<span data-ttu-id="1e9d3-134">Nome di un account di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-134">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="1e9d3-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="1e9d3-135">-Tag</span></span>
<span data-ttu-id="1e9d3-136">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-136">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="1e9d3-137">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="1e9d3-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e9d3-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1e9d3-138">-Confirm</span></span>
<span data-ttu-id="1e9d3-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e9d3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e9d3-140">-WhatIf</span></span>
<span data-ttu-id="1e9d3-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e9d3-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e9d3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e9d3-143">CommonParameters</span></span>
<span data-ttu-id="1e9d3-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e9d3-145">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e9d3-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e9d3-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1e9d3-146">INPUTS</span></span>

### <span data-ttu-id="1e9d3-147">System. String</span><span class="sxs-lookup"><span data-stu-id="1e9d3-147">System.String</span></span>

## <span data-ttu-id="1e9d3-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e9d3-148">OUTPUTS</span></span>

### <span data-ttu-id="1e9d3-149">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1e9d3-149">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="1e9d3-150">Note</span><span class="sxs-lookup"><span data-stu-id="1e9d3-150">NOTES</span></span>

## <span data-ttu-id="1e9d3-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e9d3-151">RELATED LINKS</span></span>

[<span data-ttu-id="1e9d3-152">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1e9d3-152">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="1e9d3-153">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1e9d3-153">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="1e9d3-154">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1e9d3-154">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

