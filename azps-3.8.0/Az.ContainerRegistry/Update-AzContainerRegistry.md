---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: 606f92a3cc75deb40b3781b3578e38794ae65b2b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864514"
---
# <span data-ttu-id="fb7da-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fb7da-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="fb7da-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb7da-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7da-103">Aggiorna un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="fb7da-103">Updates a container registry.</span></span>

## <span data-ttu-id="fb7da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb7da-104">SYNTAX</span></span>

### <span data-ttu-id="fb7da-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fb7da-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb7da-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb7da-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb7da-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb7da-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7da-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb7da-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7da-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb7da-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb7da-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb7da-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb7da-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb7da-111">DESCRIPTION</span></span>
<span data-ttu-id="fb7da-112">Il cmdlet Update-AzContainerRegistry aggiorna un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="fb7da-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="fb7da-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb7da-113">EXAMPLES</span></span>

### <span data-ttu-id="fb7da-114">Esempio 1: abilitare l'utente dell'amministratore per un registro contenitore specificato</span><span class="sxs-lookup"><span data-stu-id="fb7da-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="fb7da-115">Questo comando consente all'utente di amministratore per il registro di sistema contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="fb7da-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="fb7da-116">Esempio 2: impostare l'account di archiviazione usato da un registro dei contenitori specificato</span><span class="sxs-lookup"><span data-stu-id="fb7da-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="fb7da-117">Questo comando imposta il registro di sistema del contenitore specificato per l'uso di un account di archiviazione esistente \` mystorageaccount \` nella stessa sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="fb7da-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="fb7da-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb7da-118">PARAMETERS</span></span>

### <span data-ttu-id="fb7da-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7da-119">-DefaultProfile</span></span>
<span data-ttu-id="fb7da-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fb7da-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb7da-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="fb7da-121">-DisableAdminUser</span></span>
<span data-ttu-id="fb7da-122">Abilitare l'utente amministratore per il registro dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="fb7da-122">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="fb7da-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="fb7da-123">-EnableAdminUser</span></span>
<span data-ttu-id="fb7da-124">Abilitare l'utente amministratore per il registro dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="fb7da-124">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="fb7da-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb7da-125">-Name</span></span>
<span data-ttu-id="fb7da-126">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="fb7da-126">Container Registry Name.</span></span>

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

### <span data-ttu-id="fb7da-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb7da-127">-ResourceGroupName</span></span>
<span data-ttu-id="fb7da-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fb7da-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="fb7da-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb7da-129">-ResourceId</span></span>
<span data-ttu-id="fb7da-130">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="fb7da-130">The container registry resource id</span></span>

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

### <span data-ttu-id="fb7da-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="fb7da-131">-Sku</span></span>
<span data-ttu-id="fb7da-132">SKU del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="fb7da-132">Container Registry SKU.</span></span>

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

### <span data-ttu-id="fb7da-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fb7da-133">-StorageAccountName</span></span>
<span data-ttu-id="fb7da-134">Nome di un account di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="fb7da-134">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="fb7da-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="fb7da-135">-Tag</span></span>
<span data-ttu-id="fb7da-136">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="fb7da-136">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="fb7da-137">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="fb7da-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fb7da-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fb7da-138">-Confirm</span></span>
<span data-ttu-id="fb7da-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb7da-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb7da-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb7da-140">-WhatIf</span></span>
<span data-ttu-id="fb7da-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb7da-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb7da-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb7da-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb7da-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7da-143">CommonParameters</span></span>
<span data-ttu-id="fb7da-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb7da-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7da-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb7da-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7da-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb7da-146">INPUTS</span></span>

### <span data-ttu-id="fb7da-147">System. String</span><span class="sxs-lookup"><span data-stu-id="fb7da-147">System.String</span></span>

## <span data-ttu-id="fb7da-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb7da-148">OUTPUTS</span></span>

### <span data-ttu-id="fb7da-149">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fb7da-149">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="fb7da-150">Note</span><span class="sxs-lookup"><span data-stu-id="fb7da-150">NOTES</span></span>

## <span data-ttu-id="fb7da-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb7da-151">RELATED LINKS</span></span>

[<span data-ttu-id="fb7da-152">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fb7da-152">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="fb7da-153">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fb7da-153">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="fb7da-154">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fb7da-154">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

