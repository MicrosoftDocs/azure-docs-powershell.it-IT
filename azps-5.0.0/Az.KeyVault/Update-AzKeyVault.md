---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 10a441cd1354b75a13b429c4375e7bc3fba72244
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193234"
---
# <span data-ttu-id="704fe-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="704fe-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="704fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="704fe-102">SYNOPSIS</span></span>
<span data-ttu-id="704fe-103">Aggiornare lo stato di un Vault di chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="704fe-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="704fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="704fe-104">SYNTAX</span></span>

### <span data-ttu-id="704fe-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="704fe-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="704fe-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="704fe-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="704fe-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="704fe-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="704fe-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="704fe-108">DESCRIPTION</span></span>
<span data-ttu-id="704fe-109">Questo cmdlet aggiorna lo stato di un Vault di chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="704fe-109">This cmdlet updates the state of an Azure key vault.</span></span>

## <span data-ttu-id="704fe-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="704fe-110">EXAMPLES</span></span>

### <span data-ttu-id="704fe-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="704fe-111">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="704fe-112">Consente di eliminare la protezione tramite la sintassi piping.</span><span class="sxs-lookup"><span data-stu-id="704fe-112">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="704fe-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="704fe-113">PARAMETERS</span></span>

### <span data-ttu-id="704fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="704fe-114">-DefaultProfile</span></span>
<span data-ttu-id="704fe-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="704fe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="704fe-116">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="704fe-116">-EnablePurgeProtection</span></span>
<span data-ttu-id="704fe-117">Abilitare la funzionalità di protezione dall'eliminazione dei rifornimenti per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="704fe-117">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="704fe-118">Una volta abilitata, non può essere disabilitata.</span><span class="sxs-lookup"><span data-stu-id="704fe-118">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="704fe-119">È necessario attivare l'opzione soft-delete.</span><span class="sxs-lookup"><span data-stu-id="704fe-119">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="704fe-120">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="704fe-120">-EnableRbacAuthorization</span></span>
<span data-ttu-id="704fe-121">Abilitare o disabilitare il Vault chiave per autorizzare le azioni dei dati tramite il controllo di accesso basato sui ruoli (RBAC).</span><span class="sxs-lookup"><span data-stu-id="704fe-121">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

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

### <span data-ttu-id="704fe-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="704fe-122">-InputObject</span></span>
<span data-ttu-id="704fe-123">Oggetto Key Vault.</span><span class="sxs-lookup"><span data-stu-id="704fe-123">Key vault object.</span></span>

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

### <span data-ttu-id="704fe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="704fe-124">-ResourceGroupName</span></span>
<span data-ttu-id="704fe-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="704fe-125">Name of the resource group.</span></span>

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

### <span data-ttu-id="704fe-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="704fe-126">-ResourceId</span></span>
<span data-ttu-id="704fe-127">ID risorsa del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="704fe-127">Resource ID of the key vault.</span></span>

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

### <span data-ttu-id="704fe-128">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="704fe-128">-VaultName</span></span>
<span data-ttu-id="704fe-129">Nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="704fe-129">Name of the key vault.</span></span>

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

### <span data-ttu-id="704fe-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="704fe-130">-Confirm</span></span>
<span data-ttu-id="704fe-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="704fe-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="704fe-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="704fe-132">-WhatIf</span></span>
<span data-ttu-id="704fe-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="704fe-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="704fe-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="704fe-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="704fe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="704fe-135">CommonParameters</span></span>
<span data-ttu-id="704fe-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="704fe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="704fe-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="704fe-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="704fe-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="704fe-138">INPUTS</span></span>

### <span data-ttu-id="704fe-139">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="704fe-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="704fe-140">System. String</span><span class="sxs-lookup"><span data-stu-id="704fe-140">System.String</span></span>

## <span data-ttu-id="704fe-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="704fe-141">OUTPUTS</span></span>

### <span data-ttu-id="704fe-142">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="704fe-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="704fe-143">Note</span><span class="sxs-lookup"><span data-stu-id="704fe-143">NOTES</span></span>

## <span data-ttu-id="704fe-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="704fe-144">RELATED LINKS</span></span>
