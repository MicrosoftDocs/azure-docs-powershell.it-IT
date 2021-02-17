---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Remove-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 6812f6da3e32fd6074dc6958568bf3bd7eddeff0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176822"
---
# <span data-ttu-id="82e02-101">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="82e02-101">Remove-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="82e02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82e02-102">SYNOPSIS</span></span>
<span data-ttu-id="82e02-103">Rimuove una chiave del Vault chiave da un'SQL gestita</span><span class="sxs-lookup"><span data-stu-id="82e02-103">Removes a Key Vault key from a SQL managed instance</span></span>

## <span data-ttu-id="82e02-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82e02-104">SYNTAX</span></span>

### <span data-ttu-id="82e02-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="82e02-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82e02-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82e02-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82e02-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82e02-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82e02-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="82e02-108">DESCRIPTION</span></span>
<span data-ttu-id="82e02-109">Il Remove-AzSqlInstanceKeyVaultKey cmdlet rimuove la chiave del Vault chiave dall'istanza gestita specificata.</span><span class="sxs-lookup"><span data-stu-id="82e02-109">The Remove-AzSqlInstanceKeyVaultKey cmdlet  removes the Key Vault key from the specified Managed Instance.</span></span> <span data-ttu-id="82e02-110">Si noti che SQL autorizzazioni dell'istanza gestita per il vault della chiave non vengono modificate.</span><span class="sxs-lookup"><span data-stu-id="82e02-110">Note that the SQL managed instance's permissions to the key's vault are not changed.</span></span> <span data-ttu-id="82e02-111">Per modificare le autorizzazioni, usare Set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="82e02-111">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span> <span data-ttu-id="82e02-112">Si noti che questo cmdlet non apporta alcuna modifica al Vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="82e02-112">Note that this cmdlet makes no changes to Key Vault.</span></span> <span data-ttu-id="82e02-113">Per rimuovere una chiave dal Vault delle chiavi, usare Remove-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="82e02-113">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="82e02-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82e02-114">EXAMPLES</span></span>

### <span data-ttu-id="82e02-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="82e02-115">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="82e02-116">Questo comando rimuove la chiave del Vault chiave con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' dall'istanza gestita specificata.</span><span class="sxs-lookup"><span data-stu-id="82e02-116">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="82e02-117">Esempio 2: Uso dell'oggetto istanza gestita</span><span class="sxs-lookup"><span data-stu-id="82e02-117">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="82e02-118">Questo comando rimuove la chiave del Vault chiave con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' dall'istanza gestita specificata.</span><span class="sxs-lookup"><span data-stu-id="82e02-118">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="82e02-119">Esempio 3: Uso dell'ID risorsa dell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="82e02-119">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="82e02-120">Questo comando rimuove la chiave del Vault chiave con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' dall'istanza gestita specificata.</span><span class="sxs-lookup"><span data-stu-id="82e02-120">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="82e02-121">Esempio 4: Uso delle piping</span><span class="sxs-lookup"><span data-stu-id="82e02-121">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Remove-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="82e02-122">Questo comando rimuove la chiave del Vault chiave con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' dall'istanza gestita specificata.</span><span class="sxs-lookup"><span data-stu-id="82e02-122">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

## <span data-ttu-id="82e02-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82e02-123">PARAMETERS</span></span>

### <span data-ttu-id="82e02-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82e02-124">-DefaultProfile</span></span>
<span data-ttu-id="82e02-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82e02-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82e02-126">-Instance</span><span class="sxs-lookup"><span data-stu-id="82e02-126">-Instance</span></span>
<span data-ttu-id="82e02-127">Oggetto di input dell'istanza</span><span class="sxs-lookup"><span data-stu-id="82e02-127">The instance input object</span></span>

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

### <span data-ttu-id="82e02-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="82e02-128">-InstanceName</span></span>
<span data-ttu-id="82e02-129">Nome dell'istanza</span><span class="sxs-lookup"><span data-stu-id="82e02-129">The instance name</span></span>

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

### <span data-ttu-id="82e02-130">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="82e02-130">-InstanceResourceId</span></span>
<span data-ttu-id="82e02-131">ID risorsa dell'istanza</span><span class="sxs-lookup"><span data-stu-id="82e02-131">The instance resource id</span></span>

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

### <span data-ttu-id="82e02-132">-KeyId</span><span class="sxs-lookup"><span data-stu-id="82e02-132">-KeyId</span></span>
<span data-ttu-id="82e02-133">ID chiave AzureKeyVault</span><span class="sxs-lookup"><span data-stu-id="82e02-133">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="82e02-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82e02-134">-ResourceGroupName</span></span>
<span data-ttu-id="82e02-135">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="82e02-135">The Resource Group Name</span></span>

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

### <span data-ttu-id="82e02-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82e02-136">-Confirm</span></span>
<span data-ttu-id="82e02-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82e02-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82e02-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82e02-138">-WhatIf</span></span>
<span data-ttu-id="82e02-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82e02-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82e02-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82e02-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82e02-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82e02-141">CommonParameters</span></span>
<span data-ttu-id="82e02-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82e02-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82e02-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="82e02-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82e02-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="82e02-144">INPUTS</span></span>

### <span data-ttu-id="82e02-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="82e02-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="82e02-146">System.String</span><span class="sxs-lookup"><span data-stu-id="82e02-146">System.String</span></span>

## <span data-ttu-id="82e02-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82e02-147">OUTPUTS</span></span>

### <span data-ttu-id="82e02-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="82e02-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="82e02-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="82e02-149">NOTES</span></span>

## <span data-ttu-id="82e02-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82e02-150">RELATED LINKS</span></span>
