---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/Get-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 05c9565152063f10fb80d04fab0264807e9f3308
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999357"
---
# <span data-ttu-id="f9ccc-101">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f9ccc-101">Get-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="f9ccc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9ccc-102">SYNOPSIS</span></span>
<span data-ttu-id="f9ccc-103">Ottiene le SQL Vault delle chiavi di un'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="f9ccc-103">Gets a SQL managed instance's Key Vault keys.</span></span>

## <span data-ttu-id="f9ccc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9ccc-104">SYNTAX</span></span>

### <span data-ttu-id="f9ccc-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f9ccc-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9ccc-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9ccc-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9ccc-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9ccc-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9ccc-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f9ccc-108">DESCRIPTION</span></span>
<span data-ttu-id="f9ccc-109">Il cmdlet Get-AzSqlInstanceKeyVaultKey cmdlet ottiene informazioni sulle chiavi del Vault delle chiavi in un'SQL gestita.</span><span class="sxs-lookup"><span data-stu-id="f9ccc-109">The Get-AzSqlInstanceKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL managed instance.</span></span> <span data-ttu-id="f9ccc-110">È possibile visualizzare tutte le chiavi in un'istanza gestita o una chiave specifica fornendo keyId.</span><span class="sxs-lookup"><span data-stu-id="f9ccc-110">You can view all keys on a managed instance or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="f9ccc-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9ccc-111">EXAMPLES</span></span>

### <span data-ttu-id="f9ccc-112">Esempio 1: Ottenere tutte le chiavi del Vault chiave</span><span class="sxs-lookup"><span data-stu-id="f9ccc-112">Example 1: Get all Key Vault keys</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="f9ccc-113">Questo comando recupera tutte le chiavi del Vault delle chiavi in un'SQL gestita.</span><span class="sxs-lookup"><span data-stu-id="f9ccc-113">This command gets all the Key Vault keys on a SQL managed instance.</span></span>

### <span data-ttu-id="f9ccc-114">Esempio 2: Ottenere una chiave specifica del Vault delle chiavi</span><span class="sxs-lookup"><span data-stu-id="f9ccc-114">Example 2: Get a specific Key Vault key</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="f9ccc-115">Questo comando ottiene la chiave del Vault chiave con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '.</span><span class="sxs-lookup"><span data-stu-id="f9ccc-115">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="f9ccc-116">Esempio 3: Uso dell'oggetto istanza</span><span class="sxs-lookup"><span data-stu-id="f9ccc-116">Example 3: Using instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -ManagedInstance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="f9ccc-117">Questo comando ottiene la chiave del Vault chiave con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '.</span><span class="sxs-lookup"><span data-stu-id="f9ccc-117">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="f9ccc-118">Esempio 4: Uso dell'ID risorsa dell'istanza</span><span class="sxs-lookup"><span data-stu-id="f9ccc-118">Example 4: Using instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="f9ccc-119">Questo comando ottiene la chiave del Vault chiave con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '.</span><span class="sxs-lookup"><span data-stu-id="f9ccc-119">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="f9ccc-120">Esempio 5: Uso delle piping</span><span class="sxs-lookup"><span data-stu-id="f9ccc-120">Example 5: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="f9ccc-121">Questo comando ottiene la chiave del Vault chiave con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '.</span><span class="sxs-lookup"><span data-stu-id="f9ccc-121">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

## <span data-ttu-id="f9ccc-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9ccc-122">PARAMETERS</span></span>

### <span data-ttu-id="f9ccc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9ccc-123">-DefaultProfile</span></span>
<span data-ttu-id="f9ccc-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f9ccc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9ccc-125">-Instance</span><span class="sxs-lookup"><span data-stu-id="f9ccc-125">-Instance</span></span>
<span data-ttu-id="f9ccc-126">Oggetto di input dell'istanza</span><span class="sxs-lookup"><span data-stu-id="f9ccc-126">The instance input object</span></span>

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

### <span data-ttu-id="f9ccc-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="f9ccc-127">-InstanceName</span></span>
<span data-ttu-id="f9ccc-128">Nome dell'istanza</span><span class="sxs-lookup"><span data-stu-id="f9ccc-128">The instance name</span></span>

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

### <span data-ttu-id="f9ccc-129">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="f9ccc-129">-InstanceResourceId</span></span>
<span data-ttu-id="f9ccc-130">ID risorsa dell'istanza</span><span class="sxs-lookup"><span data-stu-id="f9ccc-130">The instance resource id</span></span>

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

### <span data-ttu-id="f9ccc-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="f9ccc-131">-KeyId</span></span>
<span data-ttu-id="f9ccc-132">ID chiave AzureKeyVault</span><span class="sxs-lookup"><span data-stu-id="f9ccc-132">AzureKeyVault key id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ccc-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9ccc-133">-ResourceGroupName</span></span>
<span data-ttu-id="f9ccc-134">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f9ccc-134">The Resource Group Name</span></span>

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

### <span data-ttu-id="f9ccc-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9ccc-135">-Confirm</span></span>
<span data-ttu-id="f9ccc-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9ccc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9ccc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9ccc-137">-WhatIf</span></span>
<span data-ttu-id="f9ccc-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9ccc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9ccc-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9ccc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9ccc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9ccc-140">CommonParameters</span></span>
<span data-ttu-id="f9ccc-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9ccc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9ccc-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f9ccc-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9ccc-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="f9ccc-143">INPUTS</span></span>

### <span data-ttu-id="f9ccc-144">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="f9ccc-144">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="f9ccc-145">System.String</span><span class="sxs-lookup"><span data-stu-id="f9ccc-145">System.String</span></span>

## <span data-ttu-id="f9ccc-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9ccc-146">OUTPUTS</span></span>

### <span data-ttu-id="f9ccc-147">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="f9ccc-147">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="f9ccc-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="f9ccc-148">NOTES</span></span>

## <span data-ttu-id="f9ccc-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9ccc-149">RELATED LINKS</span></span>
