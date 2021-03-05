---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/Set-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 4f3b0bccd8f352d6870899473440b690381bec10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988790"
---
# <span data-ttu-id="82f5c-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="82f5c-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="82f5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82f5c-102">SYNOPSIS</span></span>
<span data-ttu-id="82f5c-103">Imposta la protezione di TDE (Transparent Data Encryption) per un'SQL gestita.</span><span class="sxs-lookup"><span data-stu-id="82f5c-103">Sets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="82f5c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82f5c-104">SYNTAX</span></span>

### <span data-ttu-id="82f5c-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="82f5c-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82f5c-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82f5c-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-Instance] <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82f5c-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82f5c-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-InstanceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82f5c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="82f5c-108">DESCRIPTION</span></span>
<span data-ttu-id="82f5c-109">Il cmdlet Set-AzSqlInstanceTransparentDataEncryptionProtector imposta la protezione TDE per un'SQL gestita.</span><span class="sxs-lookup"><span data-stu-id="82f5c-109">The Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL managed instance.</span></span> <span data-ttu-id="82f5c-110">Modificando il tipo di protezione TDE, la protezione verrà ruotata.</span><span class="sxs-lookup"><span data-stu-id="82f5c-110">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="82f5c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82f5c-111">EXAMPLES</span></span>

### <span data-ttu-id="82f5c-112">Esempio 1: Impostare il tipo di protezione TDE (Transparent Data Encryption) su ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="82f5c-112">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type ServiceManaged

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : ServiceManaged
ManagedInstanceKeyVaultKeyName : ServiceManaged
KeyId                          :
```

<span data-ttu-id="82f5c-113">Questo comando aggiorna il tipo di protezione TDE di un'istanza gestita a Service Managed.</span><span class="sxs-lookup"><span data-stu-id="82f5c-113">This command updates a managed instance's TDE protector type to Service Managed.</span></span>

### <span data-ttu-id="82f5c-114">Esempio 2: Impostare il tipo di protezione Crittografia dati trasparente su Vault chiave di Azure</span><span class="sxs-lookup"><span data-stu-id="82f5c-114">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="82f5c-115">Questo comando aggiorna l'istanza gestita specificata in modo da usare la chiave del Vault della chiave dell'istanza gestita con ID https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' ' come protettore TDE.</span><span class="sxs-lookup"><span data-stu-id="82f5c-115">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="82f5c-116">Esempio 3: Impostare il tipo di protezione Crittografia dati trasparente su Vault chiave di Azure usando l'oggetto istanza gestita</span><span class="sxs-lookup"><span data-stu-id="82f5c-116">Example 3: Set the Transparent Data Encryption protector type to Azure Key Vault using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="82f5c-117">Questo comando aggiorna l'istanza gestita specificata in modo da usare la chiave del Vault della chiave dell'istanza gestita con ID https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' ' come protettore TDE.</span><span class="sxs-lookup"><span data-stu-id="82f5c-117">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="82f5c-118">Esempio 4: Impostare il tipo di protezione Crittografia dati trasparente su Vault chiave di Azure usando l'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="82f5c-118">Example 4: Set the Transparent Data Encryption protector type to Azure Key Vault using resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="82f5c-119">Questo comando aggiorna l'istanza gestita specificata in modo da usare la chiave del Vault della chiave dell'istanza gestita con ID https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' ' come protettore TDE.</span><span class="sxs-lookup"><span data-stu-id="82f5c-119">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="82f5c-120">Esempio 5: Impostare il tipo di protezione Della crittografia dati trasparente su Vault della chiave di Azure tramite piping</span><span class="sxs-lookup"><span data-stu-id="82f5c-120">Example 5: Set the Transparent Data Encryption protector type to Azure Key Vault using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Set-AzSqlInstanceTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="82f5c-121">Questo comando aggiorna l'istanza gestita specificata in modo da usare la chiave del Vault della chiave dell'istanza gestita con ID https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' ' come protettore TDE.</span><span class="sxs-lookup"><span data-stu-id="82f5c-121">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

## <span data-ttu-id="82f5c-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82f5c-122">PARAMETERS</span></span>

### <span data-ttu-id="82f5c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82f5c-123">-DefaultProfile</span></span>
<span data-ttu-id="82f5c-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82f5c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82f5c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="82f5c-125">-Force</span></span>
<span data-ttu-id="82f5c-126">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="82f5c-126">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="82f5c-127">-Instance</span><span class="sxs-lookup"><span data-stu-id="82f5c-127">-Instance</span></span>
<span data-ttu-id="82f5c-128">Oggetto di input dell'istanza</span><span class="sxs-lookup"><span data-stu-id="82f5c-128">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82f5c-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="82f5c-129">-InstanceName</span></span>
<span data-ttu-id="82f5c-130">Nome dell'istanza</span><span class="sxs-lookup"><span data-stu-id="82f5c-130">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f5c-131">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="82f5c-131">-InstanceResourceId</span></span>
<span data-ttu-id="82f5c-132">ID risorsa dell'istanza</span><span class="sxs-lookup"><span data-stu-id="82f5c-132">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82f5c-133">-KeyId</span><span class="sxs-lookup"><span data-stu-id="82f5c-133">-KeyId</span></span>
<span data-ttu-id="82f5c-134">KeyId del Vault della chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="82f5c-134">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f5c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82f5c-135">-ResourceGroupName</span></span>
<span data-ttu-id="82f5c-136">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="82f5c-136">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f5c-137">-Type</span><span class="sxs-lookup"><span data-stu-id="82f5c-137">-Type</span></span>
<span data-ttu-id="82f5c-138">Tipo di protezione della crittografia dei dati trasparente del database sql di Azure.</span><span class="sxs-lookup"><span data-stu-id="82f5c-138">The Azure Sql Database Transparent Data Encryption Protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f5c-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82f5c-139">-Confirm</span></span>
<span data-ttu-id="82f5c-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82f5c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82f5c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82f5c-141">-WhatIf</span></span>
<span data-ttu-id="82f5c-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82f5c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82f5c-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82f5c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82f5c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82f5c-144">CommonParameters</span></span>
<span data-ttu-id="82f5c-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82f5c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82f5c-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="82f5c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82f5c-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="82f5c-147">INPUTS</span></span>

### <span data-ttu-id="82f5c-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="82f5c-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="82f5c-149">System.String</span><span class="sxs-lookup"><span data-stu-id="82f5c-149">System.String</span></span>

## <span data-ttu-id="82f5c-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82f5c-150">OUTPUTS</span></span>

### <span data-ttu-id="82f5c-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="82f5c-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="82f5c-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="82f5c-152">NOTES</span></span>

## <span data-ttu-id="82f5c-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82f5c-153">RELATED LINKS</span></span>
