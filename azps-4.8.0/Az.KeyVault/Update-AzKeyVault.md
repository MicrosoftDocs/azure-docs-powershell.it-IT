---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 4302f2f9c4c2d6b2c7afa879fc28e2ff4edbb592
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189659"
---
# <span data-ttu-id="3a6fa-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="3a6fa-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="3a6fa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a6fa-102">SYNOPSIS</span></span>
<span data-ttu-id="3a6fa-103">Aggiornare lo stato di un Vault di chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="3a6fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a6fa-104">SYNTAX</span></span>

### <span data-ttu-id="3a6fa-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3a6fa-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a6fa-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a6fa-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a6fa-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a6fa-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a6fa-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a6fa-108">DESCRIPTION</span></span>
<span data-ttu-id="3a6fa-109">Questo cmdlet aggiorna lo stato di un Vault di chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-109">This cmdlet updates the state of an Azure key vault.</span></span>
<span data-ttu-id="3a6fa-110">Nota l'aggiornamento di alcune delle proprietà è un'azione irreversibile, ad esempio quando è stata abilitata l'eliminazione morbida, non può più essere disabilitata.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-110">Please note updating some of the properties is an irreversible action, for example once soft delete has been enabled, it cannot be disabled anymore.</span></span>

## <span data-ttu-id="3a6fa-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a6fa-111">EXAMPLES</span></span>

### <span data-ttu-id="3a6fa-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3a6fa-112">Example 1</span></span>
```powershell
PS C:\> Update-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName -EnableSoftDelete
```

<span data-ttu-id="3a6fa-113">Abilita l'eliminazione morbida nell'archivio chiavi denominato `$keyVaultName` nel gruppo risorse `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="3a6fa-113">Enables soft delete on the key vault named `$keyVaultName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="3a6fa-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3a6fa-114">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="3a6fa-115">Consente di eliminare la protezione tramite la sintassi piping.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-115">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="3a6fa-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a6fa-116">PARAMETERS</span></span>

### <span data-ttu-id="3a6fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a6fa-117">-DefaultProfile</span></span>
<span data-ttu-id="3a6fa-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a6fa-119">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="3a6fa-119">-EnablePurgeProtection</span></span>
<span data-ttu-id="3a6fa-120">Abilitare la funzionalità di protezione dall'eliminazione dei rifornimenti per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-120">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="3a6fa-121">Una volta abilitata, non può essere disabilitata.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-121">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="3a6fa-122">È necessario attivare l'opzione soft-delete.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-122">It requires soft-delete to be turned on.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a6fa-123">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="3a6fa-123">-EnableRbacAuthorization</span></span>
<span data-ttu-id="3a6fa-124">Abilitare o disabilitare il Vault chiave per autorizzare le azioni dei dati tramite il controllo di accesso basato sui ruoli (RBAC).</span><span class="sxs-lookup"><span data-stu-id="3a6fa-124">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a6fa-125">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="3a6fa-125">-EnableSoftDelete</span></span>
<span data-ttu-id="3a6fa-126">Abilitare la funzionalità di eliminazione morbida per questo Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-126">Enable the soft-delete functionality for this key vault.</span></span>
<span data-ttu-id="3a6fa-127">Una volta abilitata, non può essere disabilitata.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-127">Once enabled it cannot be disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a6fa-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a6fa-128">-InputObject</span></span>
<span data-ttu-id="3a6fa-129">Oggetto Key Vault.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-129">Key vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a6fa-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a6fa-130">-ResourceGroupName</span></span>
<span data-ttu-id="3a6fa-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-131">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a6fa-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a6fa-132">-ResourceId</span></span>
<span data-ttu-id="3a6fa-133">ID risorsa del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-133">Resource ID of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a6fa-134">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="3a6fa-134">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="3a6fa-135">Specifica il periodo di conservazione delle risorse eliminate e la durata della cancellazione di un Vault o di un oggetto nello stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-135">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="3a6fa-136">Il valore predefinito è 90 giorni.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-136">The default is 90 days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a6fa-137">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="3a6fa-137">-VaultName</span></span>
<span data-ttu-id="3a6fa-138">Nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-138">Name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a6fa-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3a6fa-139">-Confirm</span></span>
<span data-ttu-id="3a6fa-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a6fa-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a6fa-141">-WhatIf</span></span>
<span data-ttu-id="3a6fa-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a6fa-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a6fa-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a6fa-144">CommonParameters</span></span>
<span data-ttu-id="3a6fa-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a6fa-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a6fa-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a6fa-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a6fa-147">INPUTS</span></span>

### <span data-ttu-id="3a6fa-148">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="3a6fa-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="3a6fa-149">System. String</span><span class="sxs-lookup"><span data-stu-id="3a6fa-149">System.String</span></span>

## <span data-ttu-id="3a6fa-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a6fa-150">OUTPUTS</span></span>

### <span data-ttu-id="3a6fa-151">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="3a6fa-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="3a6fa-152">Note</span><span class="sxs-lookup"><span data-stu-id="3a6fa-152">NOTES</span></span>

## <span data-ttu-id="3a6fa-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a6fa-153">RELATED LINKS</span></span>
