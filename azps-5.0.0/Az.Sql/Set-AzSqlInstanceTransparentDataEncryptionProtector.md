---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Set-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 15462ea79b5499818d71b145e0faaa35c09baf0b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200424"
---
# <span data-ttu-id="70c57-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="70c57-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="70c57-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="70c57-102">SYNOPSIS</span></span>
<span data-ttu-id="70c57-103">Imposta la protezione di crittografia dati trasparente (Transparent Data Encryption) per un'istanza gestita da SQL.</span><span class="sxs-lookup"><span data-stu-id="70c57-103">Sets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="70c57-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70c57-104">SYNTAX</span></span>

### <span data-ttu-id="70c57-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="70c57-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70c57-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70c57-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-Instance] <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70c57-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70c57-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-InstanceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70c57-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70c57-108">DESCRIPTION</span></span>
<span data-ttu-id="70c57-109">Il cmdlet Set-AzSqlInstanceTransparentDataEncryptionProtector imposta la protezione di Transparent per un'istanza di SQL Managed.</span><span class="sxs-lookup"><span data-stu-id="70c57-109">The Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL managed instance.</span></span> <span data-ttu-id="70c57-110">La modifica del tipo di protezione di Transparent di transformazione ruota il Protector.</span><span class="sxs-lookup"><span data-stu-id="70c57-110">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="70c57-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70c57-111">EXAMPLES</span></span>

### <span data-ttu-id="70c57-112">Esempio 1: impostare il tipo di protezione Transparent Data Encryption (ServiceManaged)</span><span class="sxs-lookup"><span data-stu-id="70c57-112">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type ServiceManaged

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : ServiceManaged
ManagedInstanceKeyVaultKeyName : ServiceManaged
KeyId                          :
```

<span data-ttu-id="70c57-113">Questo comando Aggiorna il tipo di protezione Transparent transparent di un'istanza gestita a Service Managed.</span><span class="sxs-lookup"><span data-stu-id="70c57-113">This command updates a managed instance's TDE protector type to Service Managed.</span></span>

### <span data-ttu-id="70c57-114">Esempio 2: impostare il tipo di protezione di crittografia dati trasparente in Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="70c57-114">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="70c57-115">Questo comando Aggiorna l'istanza gestita specificata per usare la chiave di volta chiave dell'istanza gestita con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' come protezione di Transparent.</span><span class="sxs-lookup"><span data-stu-id="70c57-115">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="70c57-116">Esempio 3: impostare il tipo di protezione di crittografia dati trasparente in Azure Key Vault usando l'oggetto istanza gestito</span><span class="sxs-lookup"><span data-stu-id="70c57-116">Example 3: Set the Transparent Data Encryption protector type to Azure Key Vault using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="70c57-117">Questo comando Aggiorna l'istanza gestita specificata per usare la chiave di volta chiave dell'istanza gestita con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' come protezione di Transparent.</span><span class="sxs-lookup"><span data-stu-id="70c57-117">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="70c57-118">Esempio 4: impostare il tipo di protezione di crittografia dati trasparente in Azure Key Vault con ID risorsa</span><span class="sxs-lookup"><span data-stu-id="70c57-118">Example 4: Set the Transparent Data Encryption protector type to Azure Key Vault using resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="70c57-119">Questo comando Aggiorna l'istanza gestita specificata per usare la chiave di volta chiave dell'istanza gestita con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' come protezione di Transparent.</span><span class="sxs-lookup"><span data-stu-id="70c57-119">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="70c57-120">Esempio 5: impostare il tipo di protezione di crittografia dati trasparente in Azure Key Vault tramite piping</span><span class="sxs-lookup"><span data-stu-id="70c57-120">Example 5: Set the Transparent Data Encryption protector type to Azure Key Vault using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Set-AzSqlInstanceTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="70c57-121">Questo comando Aggiorna l'istanza gestita specificata per usare la chiave di volta chiave dell'istanza gestita con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' come protezione di Transparent.</span><span class="sxs-lookup"><span data-stu-id="70c57-121">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

## <span data-ttu-id="70c57-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="70c57-122">PARAMETERS</span></span>

### <span data-ttu-id="70c57-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70c57-123">-DefaultProfile</span></span>
<span data-ttu-id="70c57-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="70c57-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70c57-125">-Force</span><span class="sxs-lookup"><span data-stu-id="70c57-125">-Force</span></span>
<span data-ttu-id="70c57-126">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="70c57-126">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="70c57-127">-Instance</span><span class="sxs-lookup"><span data-stu-id="70c57-127">-Instance</span></span>
<span data-ttu-id="70c57-128">Oggetto di input dell'istanza</span><span class="sxs-lookup"><span data-stu-id="70c57-128">The instance input object</span></span>

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

### <span data-ttu-id="70c57-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="70c57-129">-InstanceName</span></span>
<span data-ttu-id="70c57-130">Nome dell'istanza</span><span class="sxs-lookup"><span data-stu-id="70c57-130">The instance name</span></span>

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

### <span data-ttu-id="70c57-131">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="70c57-131">-InstanceResourceId</span></span>
<span data-ttu-id="70c57-132">ID risorsa istanza</span><span class="sxs-lookup"><span data-stu-id="70c57-132">The instance resource id</span></span>

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

### <span data-ttu-id="70c57-133">-KeyId</span><span class="sxs-lookup"><span data-stu-id="70c57-133">-KeyId</span></span>
<span data-ttu-id="70c57-134">Il Vault Key di Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="70c57-134">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="70c57-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70c57-135">-ResourceGroupName</span></span>
<span data-ttu-id="70c57-136">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="70c57-136">The Resource Group Name</span></span>

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

### <span data-ttu-id="70c57-137">-Digitare</span><span class="sxs-lookup"><span data-stu-id="70c57-137">-Type</span></span>
<span data-ttu-id="70c57-138">Tipo di protezione dei dati di Azure SQL Transparent Data Encryption.</span><span class="sxs-lookup"><span data-stu-id="70c57-138">The Azure Sql Database Transparent Data Encryption Protector type.</span></span>

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

### <span data-ttu-id="70c57-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="70c57-139">-Confirm</span></span>
<span data-ttu-id="70c57-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70c57-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70c57-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70c57-141">-WhatIf</span></span>
<span data-ttu-id="70c57-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70c57-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70c57-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70c57-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70c57-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70c57-144">CommonParameters</span></span>
<span data-ttu-id="70c57-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70c57-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70c57-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70c57-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70c57-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="70c57-147">INPUTS</span></span>

### <span data-ttu-id="70c57-148">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="70c57-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="70c57-149">System. String</span><span class="sxs-lookup"><span data-stu-id="70c57-149">System.String</span></span>

## <span data-ttu-id="70c57-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70c57-150">OUTPUTS</span></span>

### <span data-ttu-id="70c57-151">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="70c57-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="70c57-152">Note</span><span class="sxs-lookup"><span data-stu-id="70c57-152">NOTES</span></span>

## <span data-ttu-id="70c57-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70c57-153">RELATED LINKS</span></span>
