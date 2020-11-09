---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: 22dfee058a26163206c973f664615a4f29ae61de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299616"
---
# <span data-ttu-id="63e1e-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="63e1e-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="63e1e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="63e1e-102">SYNOPSIS</span></span>
<span data-ttu-id="63e1e-103">Aggiorna un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="63e1e-103">Updates a container registry.</span></span>

## <span data-ttu-id="63e1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63e1e-104">SYNTAX</span></span>

### <span data-ttu-id="63e1e-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="63e1e-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e1e-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="63e1e-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e1e-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="63e1e-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e1e-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63e1e-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e1e-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63e1e-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e1e-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63e1e-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63e1e-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63e1e-111">DESCRIPTION</span></span>
<span data-ttu-id="63e1e-112">Il cmdlet Update-AzContainerRegistry aggiorna un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="63e1e-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="63e1e-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63e1e-113">EXAMPLES</span></span>

### <span data-ttu-id="63e1e-114">Esempio 1: abilitare l'utente dell'amministratore per un registro contenitore specificato</span><span class="sxs-lookup"><span data-stu-id="63e1e-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="63e1e-115">Questo comando consente all'utente di amministratore per il registro di sistema contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="63e1e-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="63e1e-116">Esempio 2: impostare l'account di archiviazione usato da un registro dei contenitori specificato</span><span class="sxs-lookup"><span data-stu-id="63e1e-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="63e1e-117">Questo comando imposta il registro di sistema del contenitore specificato per l'uso di un account di archiviazione esistente \` mystorageaccount \` nella stessa sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="63e1e-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="63e1e-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="63e1e-118">PARAMETERS</span></span>

### <span data-ttu-id="63e1e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e1e-119">-DefaultProfile</span></span>
<span data-ttu-id="63e1e-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="63e1e-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63e1e-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="63e1e-121">-DisableAdminUser</span></span>
<span data-ttu-id="63e1e-122">Abilitare l'utente amministratore per il registro dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="63e1e-122">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="63e1e-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="63e1e-123">-EnableAdminUser</span></span>
<span data-ttu-id="63e1e-124">Abilitare l'utente amministratore per il registro dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="63e1e-124">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="63e1e-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="63e1e-125">-Name</span></span>
<span data-ttu-id="63e1e-126">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="63e1e-126">Container Registry Name.</span></span>

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

### <span data-ttu-id="63e1e-127">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="63e1e-127">-NetworkRuleSet</span></span>
<span data-ttu-id="63e1e-128">Set di regole di rete per un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="63e1e-128">The network rule set for a container registry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63e1e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63e1e-129">-ResourceGroupName</span></span>
<span data-ttu-id="63e1e-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="63e1e-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="63e1e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63e1e-131">-ResourceId</span></span>
<span data-ttu-id="63e1e-132">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="63e1e-132">The container registry resource id</span></span>

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

### <span data-ttu-id="63e1e-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="63e1e-133">-Sku</span></span>
<span data-ttu-id="63e1e-134">SKU del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="63e1e-134">Container Registry SKU.</span></span>

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

### <span data-ttu-id="63e1e-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="63e1e-135">-StorageAccountName</span></span>
<span data-ttu-id="63e1e-136">Nome di un account di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="63e1e-136">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="63e1e-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="63e1e-137">-Tag</span></span>
<span data-ttu-id="63e1e-138">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="63e1e-138">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="63e1e-139">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="63e1e-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="63e1e-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="63e1e-140">-Confirm</span></span>
<span data-ttu-id="63e1e-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63e1e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63e1e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63e1e-142">-WhatIf</span></span>
<span data-ttu-id="63e1e-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63e1e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63e1e-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63e1e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63e1e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e1e-145">CommonParameters</span></span>
<span data-ttu-id="63e1e-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63e1e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e1e-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63e1e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e1e-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="63e1e-148">INPUTS</span></span>

### <span data-ttu-id="63e1e-149">System. String</span><span class="sxs-lookup"><span data-stu-id="63e1e-149">System.String</span></span>

## <span data-ttu-id="63e1e-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63e1e-150">OUTPUTS</span></span>

### <span data-ttu-id="63e1e-151">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="63e1e-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="63e1e-152">Note</span><span class="sxs-lookup"><span data-stu-id="63e1e-152">NOTES</span></span>

## <span data-ttu-id="63e1e-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63e1e-153">RELATED LINKS</span></span>

[<span data-ttu-id="63e1e-154">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="63e1e-154">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="63e1e-155">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="63e1e-155">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="63e1e-156">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="63e1e-156">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

