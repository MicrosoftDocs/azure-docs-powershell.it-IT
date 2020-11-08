---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 0ceaf3906860916c4740c3d06d1c9ee91be421cb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193160"
---
# <span data-ttu-id="6cba0-101">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6cba0-101">Add-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="6cba0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6cba0-102">SYNOPSIS</span></span>
<span data-ttu-id="6cba0-103">Aggiunge una chiave del Vault Key all'istanza gestita specificata.</span><span class="sxs-lookup"><span data-stu-id="6cba0-103">Adds a key vault key to the provided Managed Instance.</span></span> 

## <span data-ttu-id="6cba0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6cba0-104">SYNTAX</span></span>

### <span data-ttu-id="6cba0-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6cba0-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cba0-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cba0-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cba0-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cba0-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cba0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6cba0-108">DESCRIPTION</span></span>
<span data-ttu-id="6cba0-109">Il cmdlet Add-AzSqlInstanceKeyVaultKey aggiunge una chiave di volta chiave all'istanza gestita specificata.</span><span class="sxs-lookup"><span data-stu-id="6cba0-109">The Add-AzSqlInstanceKeyVaultKey cmdlet adds a key vault key to the provided Managed Instance.</span></span> <span data-ttu-id="6cba0-110">L'istanza gestita deve avere le autorizzazioni ' Get, wrapKey, unwrapKey ' per il Vault, USA lo script seguente per concedere l'autorizzazione all'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="6cba0-110">The managed instance must have 'get, wrapKey, unwrapKey' permissions to the vault, use the following script to grant permission to the managed instance.</span></span>
<span data-ttu-id="6cba0-111">$managedInstance = Get-AzSqlInstance-Name ' ContosoManagedInstanceName '-ResourceGroupName ' ContosoResourceGroup ' Set-AzKeyVaultAccessPolicy-VAULTNAME ContosoVault-ObjectId $managedInstance. Identity. PrincipalId-PermissionsToKeys Get, wrapKey, unwrapKey</span><span class="sxs-lookup"><span data-stu-id="6cba0-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span></span>

## <span data-ttu-id="6cba0-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6cba0-112">EXAMPLES</span></span>

### <span data-ttu-id="6cba0-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6cba0-113">Example 1</span></span>
```powershell
PS C:\> Add-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="6cba0-114">Questo comando aggiunge la chiave di volta chiave con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' all'istanza di SQL Managed denominata "ContosoManagedInstanceName" nel gruppo di risorse "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="6cba0-114">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="6cba0-115">Esempio 2: uso dell'oggetto istanza gestito</span><span class="sxs-lookup"><span data-stu-id="6cba0-115">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="6cba0-116">Questo comando aggiunge la chiave di volta chiave con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' all'istanza di SQL Managed denominata "ContosoManagedInstanceName" nel gruppo di risorse "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="6cba0-116">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="6cba0-117">Esempio 3: uso dell'ID risorsa istanza gestita</span><span class="sxs-lookup"><span data-stu-id="6cba0-117">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="6cba0-118">Questo comando aggiunge la chiave di volta chiave con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' all'istanza di SQL Managed denominata "ContosoManagedInstanceName" nel gruppo di risorse "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="6cba0-118">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="6cba0-119">Esempio 4: utilizzo di piping</span><span class="sxs-lookup"><span data-stu-id="6cba0-119">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Add-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="6cba0-120">Questo comando aggiunge la chiave di volta chiave con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' all'istanza di SQL Managed denominata "ContosoManagedInstanceName" nel gruppo di risorse "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="6cba0-120">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

## <span data-ttu-id="6cba0-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6cba0-121">PARAMETERS</span></span>

### <span data-ttu-id="6cba0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cba0-122">-DefaultProfile</span></span>
<span data-ttu-id="6cba0-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6cba0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cba0-124">-Instance</span><span class="sxs-lookup"><span data-stu-id="6cba0-124">-Instance</span></span>
<span data-ttu-id="6cba0-125">Oggetto di input dell'istanza</span><span class="sxs-lookup"><span data-stu-id="6cba0-125">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cba0-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="6cba0-126">-InstanceName</span></span>
<span data-ttu-id="6cba0-127">Nome dell'istanza</span><span class="sxs-lookup"><span data-stu-id="6cba0-127">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cba0-128">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="6cba0-128">-InstanceResourceId</span></span>
<span data-ttu-id="6cba0-129">ID risorsa istanza</span><span class="sxs-lookup"><span data-stu-id="6cba0-129">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cba0-130">-KeyId</span><span class="sxs-lookup"><span data-stu-id="6cba0-130">-KeyId</span></span>
<span data-ttu-id="6cba0-131">ID chiave AzureKeyVault</span><span class="sxs-lookup"><span data-stu-id="6cba0-131">AzureKeyVault key id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cba0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cba0-132">-ResourceGroupName</span></span>
<span data-ttu-id="6cba0-133">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6cba0-133">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cba0-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6cba0-134">-Confirm</span></span>
<span data-ttu-id="6cba0-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cba0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cba0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cba0-136">-WhatIf</span></span>
<span data-ttu-id="6cba0-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6cba0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cba0-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6cba0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cba0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cba0-139">CommonParameters</span></span>
<span data-ttu-id="6cba0-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cba0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cba0-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cba0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cba0-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6cba0-142">INPUTS</span></span>

### <span data-ttu-id="6cba0-143">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="6cba0-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="6cba0-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6cba0-144">System.String</span></span>

## <span data-ttu-id="6cba0-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6cba0-145">OUTPUTS</span></span>

### <span data-ttu-id="6cba0-146">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="6cba0-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="6cba0-147">Note</span><span class="sxs-lookup"><span data-stu-id="6cba0-147">NOTES</span></span>

## <span data-ttu-id="6cba0-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6cba0-148">RELATED LINKS</span></span>