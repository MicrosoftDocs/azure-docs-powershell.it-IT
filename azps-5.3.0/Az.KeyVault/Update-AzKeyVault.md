---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 2a9c2870e0ce33b93d3013e84e7de3642b42708c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473703"
---
# <span data-ttu-id="0eb4e-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="0eb4e-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="0eb4e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0eb4e-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb4e-103">Aggiornare lo stato di un Vault di chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="0eb4e-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="0eb4e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0eb4e-104">SYNTAX</span></span>

### <span data-ttu-id="0eb4e-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0eb4e-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eb4e-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0eb4e-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eb4e-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0eb4e-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eb4e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0eb4e-108">DESCRIPTION</span></span>
<span data-ttu-id="0eb4e-109">Questo cmdlet aggiorna lo stato di un Vault di chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="0eb4e-109">This cmdlet updates the state of an Azure key vault.</span></span>

## <span data-ttu-id="0eb4e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0eb4e-110">EXAMPLES</span></span>

### <span data-ttu-id="0eb4e-111">Esempio 1: abilitare la protezione dall'eliminazione</span><span class="sxs-lookup"><span data-stu-id="0eb4e-111">Example 1： Enable purge protection</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="0eb4e-112">Consente di eliminare la protezione tramite la sintassi piping.</span><span class="sxs-lookup"><span data-stu-id="0eb4e-112">Enables purge protection using piping syntax.</span></span>

### <span data-ttu-id="0eb4e-113">Esempio 2: abilitare l'autorizzazione RBAC</span><span class="sxs-lookup"><span data-stu-id="0eb4e-113">Example 2： Enable RBAC Authorization</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnableRbacAuthorization $true
```

<span data-ttu-id="0eb4e-114">Abilita l'autorizzazione RBAC usando la sintassi piping.</span><span class="sxs-lookup"><span data-stu-id="0eb4e-114">Enables RBAC Authorization using piping syntax.</span></span>

### <span data-ttu-id="0eb4e-115">Esempio 3: impostare i tag</span><span class="sxs-lookup"><span data-stu-id="0eb4e-115">Example 3： Set tags</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName | Update-AzKeyVault -Tags @{key = "value"}
```

<span data-ttu-id="0eb4e-116">Imposta i tag di un Vault chiave denominato $keyVaultName.</span><span class="sxs-lookup"><span data-stu-id="0eb4e-116">Sets the tags of a key vault named $keyVaultName.</span></span>

### <span data-ttu-id="0eb4e-117">Esempio 4: pulire i tag</span><span class="sxs-lookup"><span data-stu-id="0eb4e-117">Example 4： Clean tags</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName | Update-AzKeyVault -Tags @{}
```

<span data-ttu-id="0eb4e-118">Elimina tutti i tag di un Vault chiave denominato $keyVaultName.</span><span class="sxs-lookup"><span data-stu-id="0eb4e-118">Deletes all tags of a key vault named $keyVaultName.</span></span>

## <span data-ttu-id="0eb4e-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0eb4e-119">PARAMETERS</span></span>

### <span data-ttu-id="0eb4e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb4e-120">-DefaultProfile</span></span>
<span data-ttu-id="0eb4e-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0eb4e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0eb4e-122">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="0eb4e-122">-EnablePurgeProtection</span></span>
<span data-ttu-id="0eb4e-123">Abilitare la funzionalità di protezione dall'eliminazione dei rifornimenti per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="0eb4e-123">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="0eb4e-124">Una volta abilitata, non può essere disabilitata.</span><span class="sxs-lookup"><span data-stu-id="0eb4e-124">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="0eb4e-125">È necessario attivare l'opzione soft-delete.</span><span class="sxs-lookup"><span data-stu-id="0eb4e-125">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="0eb4e-126">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="0eb4e-126">-EnableRbacAuthorization</span></span>
<span data-ttu-id="0eb4e-127">Abilitare o disabilitare il Vault chiave per autorizzare le azioni dei dati tramite il controllo di accesso basato sui ruoli (RBAC).</span><span class="sxs-lookup"><span data-stu-id="0eb4e-127">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

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

### <span data-ttu-id="0eb4e-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0eb4e-128">-InputObject</span></span>
<span data-ttu-id="0eb4e-129">Oggetto Key Vault.</span><span class="sxs-lookup"><span data-stu-id="0eb4e-129">Key vault object.</span></span>

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

### <span data-ttu-id="0eb4e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eb4e-130">-ResourceGroupName</span></span>
<span data-ttu-id="0eb4e-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0eb4e-131">Name of the resource group.</span></span>

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

### <span data-ttu-id="0eb4e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0eb4e-132">-ResourceId</span></span>
<span data-ttu-id="0eb4e-133">ID risorsa del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="0eb4e-133">Resource ID of the key vault.</span></span>

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

### <span data-ttu-id="0eb4e-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="0eb4e-134">-Tag</span></span>
<span data-ttu-id="0eb4e-135">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="0eb4e-135">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb4e-136">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="0eb4e-136">-VaultName</span></span>
<span data-ttu-id="0eb4e-137">Nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="0eb4e-137">Name of the key vault.</span></span>

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

### <span data-ttu-id="0eb4e-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0eb4e-138">-Confirm</span></span>
<span data-ttu-id="0eb4e-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eb4e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eb4e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eb4e-140">-WhatIf</span></span>
<span data-ttu-id="0eb4e-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0eb4e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eb4e-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0eb4e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eb4e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb4e-143">CommonParameters</span></span>
<span data-ttu-id="0eb4e-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eb4e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb4e-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0eb4e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb4e-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0eb4e-146">INPUTS</span></span>

### <span data-ttu-id="0eb4e-147">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0eb4e-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="0eb4e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="0eb4e-148">System.String</span></span>

## <span data-ttu-id="0eb4e-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0eb4e-149">OUTPUTS</span></span>

### <span data-ttu-id="0eb4e-150">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0eb4e-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="0eb4e-151">Note</span><span class="sxs-lookup"><span data-stu-id="0eb4e-151">NOTES</span></span>

## <span data-ttu-id="0eb4e-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0eb4e-152">RELATED LINKS</span></span>
