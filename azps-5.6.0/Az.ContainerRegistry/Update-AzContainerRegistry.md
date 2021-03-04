---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: aa84186be2b5dc13117397e76722a6826d5314a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956317"
---
# <span data-ttu-id="e2a6f-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e2a6f-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="e2a6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2a6f-102">SYNOPSIS</span></span>
<span data-ttu-id="e2a6f-103">Aggiorna un registro di contenitore.</span><span class="sxs-lookup"><span data-stu-id="e2a6f-103">Updates a container registry.</span></span>

## <span data-ttu-id="e2a6f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2a6f-104">SYNTAX</span></span>

### <span data-ttu-id="e2a6f-105">NameResourceGroupParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e2a6f-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2a6f-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2a6f-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2a6f-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2a6f-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2a6f-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2a6f-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2a6f-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2a6f-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2a6f-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2a6f-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2a6f-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e2a6f-111">DESCRIPTION</span></span>
<span data-ttu-id="e2a6f-112">Il cmdlet Update-AzContainerRegistry aggiorna il Registro di sistema di un contenitore.</span><span class="sxs-lookup"><span data-stu-id="e2a6f-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="e2a6f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2a6f-113">EXAMPLES</span></span>

### <span data-ttu-id="e2a6f-114">Esempio 1: Abilitare un utente amministratore per un contenitore specificato nel Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="e2a6f-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="e2a6f-115">Questo comando abilita l'utente amministratore per il Registro di sistema del contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="e2a6f-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="e2a6f-116">Esempio 2: Impostare l'account di archiviazione usato da un contenitore specificato nel Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="e2a6f-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="e2a6f-117">Questo comando imposta il Registro di sistema del contenitore specificato in modo da usare un account di archiviazione \` esistente nella \` stessa sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="e2a6f-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="e2a6f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2a6f-118">PARAMETERS</span></span>

### <span data-ttu-id="e2a6f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2a6f-119">-DefaultProfile</span></span>
<span data-ttu-id="e2a6f-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e2a6f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2a6f-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="e2a6f-121">-DisableAdminUser</span></span>
<span data-ttu-id="e2a6f-122">Abilitare l'utente amministratore per il Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="e2a6f-122">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="e2a6f-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="e2a6f-123">-EnableAdminUser</span></span>
<span data-ttu-id="e2a6f-124">Abilitare l'utente amministratore per il Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="e2a6f-124">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="e2a6f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e2a6f-125">-Name</span></span>
<span data-ttu-id="e2a6f-126">Nome del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="e2a6f-126">Container Registry Name.</span></span>

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

### <span data-ttu-id="e2a6f-127">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2a6f-127">-NetworkRuleSet</span></span>
<span data-ttu-id="e2a6f-128">Set di regole di rete per un registro dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="e2a6f-128">The network rule set for a container registry.</span></span>

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

### <span data-ttu-id="e2a6f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2a6f-129">-ResourceGroupName</span></span>
<span data-ttu-id="e2a6f-130">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e2a6f-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="e2a6f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2a6f-131">-ResourceId</span></span>
<span data-ttu-id="e2a6f-132">ID risorsa del Registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="e2a6f-132">The container registry resource id</span></span>

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

### <span data-ttu-id="e2a6f-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="e2a6f-133">-Sku</span></span>
<span data-ttu-id="e2a6f-134">SKU del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="e2a6f-134">Container Registry SKU.</span></span>

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

### <span data-ttu-id="e2a6f-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e2a6f-135">-StorageAccountName</span></span>
<span data-ttu-id="e2a6f-136">Nome di un account di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="e2a6f-136">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="e2a6f-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="e2a6f-137">-Tag</span></span>
<span data-ttu-id="e2a6f-138">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e2a6f-138">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="e2a6f-139">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="e2a6f-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e2a6f-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2a6f-140">-Confirm</span></span>
<span data-ttu-id="e2a6f-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2a6f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2a6f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2a6f-142">-WhatIf</span></span>
<span data-ttu-id="e2a6f-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2a6f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2a6f-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2a6f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2a6f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2a6f-145">CommonParameters</span></span>
<span data-ttu-id="e2a6f-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2a6f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2a6f-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e2a6f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2a6f-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="e2a6f-148">INPUTS</span></span>

### <span data-ttu-id="e2a6f-149">System.String</span><span class="sxs-lookup"><span data-stu-id="e2a6f-149">System.String</span></span>

## <span data-ttu-id="e2a6f-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2a6f-150">OUTPUTS</span></span>

### <span data-ttu-id="e2a6f-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e2a6f-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="e2a6f-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="e2a6f-152">NOTES</span></span>

## <span data-ttu-id="e2a6f-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2a6f-153">RELATED LINKS</span></span>

[<span data-ttu-id="e2a6f-154">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e2a6f-154">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="e2a6f-155">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e2a6f-155">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="e2a6f-156">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e2a6f-156">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

