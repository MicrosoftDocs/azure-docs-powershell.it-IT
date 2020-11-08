---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsm.md
ms.openlocfilehash: 49e8e5aeddba1b15c97155a200413ea774c8a7a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203649"
---
# <span data-ttu-id="f521c-101">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f521c-101">Update-AzManagedHsm</span></span>

## <span data-ttu-id="f521c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f521c-102">SYNOPSIS</span></span>
<span data-ttu-id="f521c-103">Aggiornare lo stato di un HSM gestito di Azure.</span><span class="sxs-lookup"><span data-stu-id="f521c-103">Update the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="f521c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f521c-104">SYNTAX</span></span>

### <span data-ttu-id="f521c-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f521c-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzManagedHsm -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f521c-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f521c-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzManagedHsm -InputObject <PSManagedHsm> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f521c-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f521c-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzManagedHsm -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f521c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f521c-108">DESCRIPTION</span></span>
<span data-ttu-id="f521c-109">Questo cmdlet aggiorna lo stato di un HSM gestito di Azure.</span><span class="sxs-lookup"><span data-stu-id="f521c-109">This cmdlet updates the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="f521c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f521c-110">EXAMPLES</span></span>

### <span data-ttu-id="f521c-111">Esempio 1: aggiornare direttamente un HSM gestito</span><span class="sxs-lookup"><span data-stu-id="f521c-111">Example 1: Update a managed Hsm directly</span></span>
```powershell
PS C:\> Update-AzManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName -Tag @{testKey="testValue"} | fl

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

<span data-ttu-id="f521c-112">Aggiorna i tag per l'HSM gestito denominato `$hsmName` nel gruppo risorse `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="f521c-112">Updates tags for the managed Hsm named `$hsmName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="f521c-113">Esempio 2: aggiornare un HSM gestito tramite piping</span><span class="sxs-lookup"><span data-stu-id="f521c-113">Example 2: Update a managed Hsm using piping</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName | Update-AzManagedHsm -Tag @{testKey="testValue"}
```

<span data-ttu-id="f521c-114">Aggiorna i tag per l'HSM gestito usando la sintassi piping.</span><span class="sxs-lookup"><span data-stu-id="f521c-114">Updates tags for the managed Hsm using piping syntax.</span></span>

## <span data-ttu-id="f521c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f521c-115">PARAMETERS</span></span>

### <span data-ttu-id="f521c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f521c-116">-DefaultProfile</span></span>
<span data-ttu-id="f521c-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f521c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f521c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f521c-118">-InputObject</span></span>
<span data-ttu-id="f521c-119">Oggetto HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="f521c-119">Managed HSM object.</span></span>

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

### <span data-ttu-id="f521c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f521c-120">-Name</span></span>
<span data-ttu-id="f521c-121">Nome dell'HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="f521c-121">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="f521c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f521c-122">-ResourceGroupName</span></span>
<span data-ttu-id="f521c-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f521c-123">Name of the resource group.</span></span>

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

### <span data-ttu-id="f521c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f521c-124">-ResourceId</span></span>
<span data-ttu-id="f521c-125">ID risorsa dell'HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="f521c-125">Resource ID of the managed HSM.</span></span>

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

### <span data-ttu-id="f521c-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="f521c-126">-Tag</span></span>
<span data-ttu-id="f521c-127">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="f521c-127">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="f521c-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f521c-128">-Confirm</span></span>
<span data-ttu-id="f521c-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f521c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f521c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f521c-130">-WhatIf</span></span>
<span data-ttu-id="f521c-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f521c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f521c-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f521c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f521c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f521c-133">CommonParameters</span></span>
<span data-ttu-id="f521c-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f521c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f521c-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f521c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f521c-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f521c-136">INPUTS</span></span>

### <span data-ttu-id="f521c-137">Microsoft. Azure. Commands. Vault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f521c-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="f521c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f521c-138">System.String</span></span>

### <span data-ttu-id="f521c-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f521c-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f521c-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f521c-140">OUTPUTS</span></span>

### <span data-ttu-id="f521c-141">Microsoft. Azure. Commands. Vault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f521c-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="f521c-142">Note</span><span class="sxs-lookup"><span data-stu-id="f521c-142">NOTES</span></span>

## <span data-ttu-id="f521c-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f521c-143">RELATED LINKS</span></span>

[<span data-ttu-id="f521c-144">New-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f521c-144">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="f521c-145">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f521c-145">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="f521c-146">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f521c-146">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)