---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 8932402fb9e4e6b27f284313bfddc764192c5e93
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864697"
---
# <span data-ttu-id="1ea5e-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="1ea5e-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="1ea5e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1ea5e-102">SYNOPSIS</span></span>
<span data-ttu-id="1ea5e-103">Aggiornare lo stato di un Vault di chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="1ea5e-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="1ea5e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ea5e-104">SYNTAX</span></span>

### <span data-ttu-id="1ea5e-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1ea5e-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ea5e-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ea5e-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ea5e-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ea5e-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ea5e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ea5e-108">DESCRIPTION</span></span>
<span data-ttu-id="1ea5e-109">Questo cmdlet aggiorna lo stato di un Vault di chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="1ea5e-109">This cmdlet updates the state of an Azure key vault.</span></span>
<span data-ttu-id="1ea5e-110">Nota l'aggiornamento di alcune delle proprietà è un'azione irreversibile, ad esempio quando è stata abilitata l'eliminazione morbida, non può più essere disabilitata.</span><span class="sxs-lookup"><span data-stu-id="1ea5e-110">Please note updating some of the properties is an irreversible action, for example once soft delete has been enabled, it cannot be disabled anymore.</span></span>

## <span data-ttu-id="1ea5e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ea5e-111">EXAMPLES</span></span>

### <span data-ttu-id="1ea5e-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1ea5e-112">Example 1</span></span>
```powershell
PS C:\> Update-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName -EnableSoftDelete
```

<span data-ttu-id="1ea5e-113">Abilita l'eliminazione morbida nell'archivio chiavi denominato `$keyVaultName` nel gruppo risorse `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="1ea5e-113">Enables soft delete on the key vault named `$keyVaultName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="1ea5e-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1ea5e-114">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="1ea5e-115">Consente di eliminare la protezione tramite la sintassi piping.</span><span class="sxs-lookup"><span data-stu-id="1ea5e-115">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="1ea5e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1ea5e-116">PARAMETERS</span></span>

### <span data-ttu-id="1ea5e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ea5e-117">-DefaultProfile</span></span>
<span data-ttu-id="1ea5e-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ea5e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea5e-119">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="1ea5e-119">-EnablePurgeProtection</span></span>
<span data-ttu-id="1ea5e-120">Abilitare la funzionalità di protezione dall'eliminazione dei rifornimenti per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="1ea5e-120">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="1ea5e-121">Una volta abilitata, non può essere disabilitata.</span><span class="sxs-lookup"><span data-stu-id="1ea5e-121">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="1ea5e-122">È necessario attivare l'opzione soft-delete.</span><span class="sxs-lookup"><span data-stu-id="1ea5e-122">It requires soft-delete to be turned on.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea5e-123">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="1ea5e-123">-EnableSoftDelete</span></span>
<span data-ttu-id="1ea5e-124">Abilitare la funzionalità di eliminazione morbida per questo Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="1ea5e-124">Enable the soft-delete functionality for this key vault.</span></span>
<span data-ttu-id="1ea5e-125">Una volta abilitata, non può essere disabilitata.</span><span class="sxs-lookup"><span data-stu-id="1ea5e-125">Once enabled it cannot be disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea5e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ea5e-126">-InputObject</span></span>
<span data-ttu-id="1ea5e-127">Oggetto Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1ea5e-127">Key vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ea5e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ea5e-128">-ResourceGroupName</span></span>
<span data-ttu-id="1ea5e-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1ea5e-129">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea5e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ea5e-130">-ResourceId</span></span>
<span data-ttu-id="1ea5e-131">ID risorsa del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="1ea5e-131">Resource ID of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ea5e-132">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="1ea5e-132">-VaultName</span></span>
<span data-ttu-id="1ea5e-133">Nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="1ea5e-133">Name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea5e-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1ea5e-134">-Confirm</span></span>
<span data-ttu-id="1ea5e-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ea5e-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea5e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ea5e-136">-WhatIf</span></span>
<span data-ttu-id="1ea5e-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ea5e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ea5e-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ea5e-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea5e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ea5e-139">CommonParameters</span></span>
<span data-ttu-id="1ea5e-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ea5e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ea5e-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ea5e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ea5e-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1ea5e-142">INPUTS</span></span>

### <span data-ttu-id="1ea5e-143">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="1ea5e-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="1ea5e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="1ea5e-144">System.String</span></span>

## <span data-ttu-id="1ea5e-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ea5e-145">OUTPUTS</span></span>

### <span data-ttu-id="1ea5e-146">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="1ea5e-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="1ea5e-147">Note</span><span class="sxs-lookup"><span data-stu-id="1ea5e-147">NOTES</span></span>

## <span data-ttu-id="1ea5e-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ea5e-148">RELATED LINKS</span></span>
