---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 6f4ddcb358c2ebc0789bb96508feacb69449d17d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976957"
---
# <span data-ttu-id="01b52-101">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="01b52-101">Update-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="01b52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01b52-102">SYNOPSIS</span></span>
<span data-ttu-id="01b52-103">Aggiornare lo stato di un servizio HSM gestito da Azure.</span><span class="sxs-lookup"><span data-stu-id="01b52-103">Update the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="01b52-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01b52-104">SYNTAX</span></span>

### <span data-ttu-id="01b52-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="01b52-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVaultManagedHsm -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01b52-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01b52-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVaultManagedHsm -InputObject <PSManagedHsm> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01b52-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01b52-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVaultManagedHsm -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01b52-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="01b52-108">DESCRIPTION</span></span>
<span data-ttu-id="01b52-109">Questo cmdlet aggiorna lo stato di un servizio HSM gestito da Azure.</span><span class="sxs-lookup"><span data-stu-id="01b52-109">This cmdlet updates the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="01b52-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01b52-110">EXAMPLES</span></span>

### <span data-ttu-id="01b52-111">Esempio 1: Aggiornare direttamente un file Hsm gestito</span><span class="sxs-lookup"><span data-stu-id="01b52-111">Example 1: Update a managed Hsm directly</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName -Tag @{testKey="testValue"} | fl

Managed HSM Name                    : testmhsm
Resource Group Name                 : testmhsm
Location                            : eastus2euap
Resource ID                         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testmhsm/provid
                                      ers/Microsoft.KeyVault/managedHSMs/testmhsm
HSM Pool URI                        :
Tenant ID                           : xxxxxx-xxxx-xxxx-xxxxxxxxxxxx
Initial Admin Object Ids            : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SKU                                 : StandardB1
Soft Delete Enabled?                : True
Enabled Purge Protection?           : False
Soft Delete Retention Period (days) : 90
Provisioning State                  : Provisioning
Status Message                      : Resource creation in progress. Starting service...
Tags                                :
                                      Name        Value
                                      ====        =====
                                      testKey     testValued
```

<span data-ttu-id="01b52-112">Aggiorna i tag per l'Hsm gestito `$hsmName` denominato nel gruppo di `$resourceGroupName` risorse.</span><span class="sxs-lookup"><span data-stu-id="01b52-112">Updates tags for the managed Hsm named `$hsmName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="01b52-113">Esempio 2: Aggiornare un'Hsm gestita tramite piping</span><span class="sxs-lookup"><span data-stu-id="01b52-113">Example 2: Update a managed Hsm using piping</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName | Update-AzKeyVaultManagedHsm -Tag @{testKey="testValue"}
```

<span data-ttu-id="01b52-114">Aggiorna i tag per l'Hsm gestito usando la sintassi di piping.</span><span class="sxs-lookup"><span data-stu-id="01b52-114">Updates tags for the managed Hsm using piping syntax.</span></span>

## <span data-ttu-id="01b52-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01b52-115">PARAMETERS</span></span>

### <span data-ttu-id="01b52-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01b52-116">-DefaultProfile</span></span>
<span data-ttu-id="01b52-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01b52-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01b52-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01b52-118">-InputObject</span></span>
<span data-ttu-id="01b52-119">Oggetto HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="01b52-119">Managed HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01b52-120">-Name</span><span class="sxs-lookup"><span data-stu-id="01b52-120">-Name</span></span>
<span data-ttu-id="01b52-121">Nome del servizio HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="01b52-121">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01b52-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01b52-122">-ResourceGroupName</span></span>
<span data-ttu-id="01b52-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="01b52-123">Name of the resource group.</span></span>

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

### <span data-ttu-id="01b52-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01b52-124">-ResourceId</span></span>
<span data-ttu-id="01b52-125">ID risorsa dell'HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="01b52-125">Resource ID of the managed HSM.</span></span>

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

### <span data-ttu-id="01b52-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="01b52-126">-Tag</span></span>
<span data-ttu-id="01b52-127">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="01b52-127">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="01b52-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01b52-128">-Confirm</span></span>
<span data-ttu-id="01b52-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01b52-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01b52-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01b52-130">-WhatIf</span></span>
<span data-ttu-id="01b52-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01b52-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01b52-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01b52-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01b52-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01b52-133">CommonParameters</span></span>
<span data-ttu-id="01b52-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01b52-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01b52-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="01b52-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01b52-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="01b52-136">INPUTS</span></span>

### <span data-ttu-id="01b52-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="01b52-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="01b52-138">System.String</span><span class="sxs-lookup"><span data-stu-id="01b52-138">System.String</span></span>

### <span data-ttu-id="01b52-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="01b52-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="01b52-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01b52-140">OUTPUTS</span></span>

### <span data-ttu-id="01b52-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="01b52-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="01b52-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="01b52-142">NOTES</span></span>

## <span data-ttu-id="01b52-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01b52-143">RELATED LINKS</span></span>

[<span data-ttu-id="01b52-144">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="01b52-144">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="01b52-145">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="01b52-145">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="01b52-146">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="01b52-146">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)