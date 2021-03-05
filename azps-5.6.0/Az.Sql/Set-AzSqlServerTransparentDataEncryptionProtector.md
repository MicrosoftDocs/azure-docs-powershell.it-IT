---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: 992601b3a6d88c7aa424564189dc8af3efe6464d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967278"
---
# <span data-ttu-id="4c15d-101">Set-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="4c15d-101">Set-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="4c15d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c15d-102">SYNOPSIS</span></span>
<span data-ttu-id="4c15d-103">Imposta la protezione di TDE (Transparent Data Encryption) per un SQL server.</span><span class="sxs-lookup"><span data-stu-id="4c15d-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

## <span data-ttu-id="4c15d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c15d-104">SYNTAX</span></span>

```
Set-AzSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c15d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4c15d-105">DESCRIPTION</span></span>
<span data-ttu-id="4c15d-106">Il Set-AzSqlServerTransparentDataEncryptionProtector cmdlet imposta la protezione TDE per un SQL server.</span><span class="sxs-lookup"><span data-stu-id="4c15d-106">The Set-AzSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="4c15d-107">Modificando il tipo di protezione TDE, la protezione verrà ruotata.</span><span class="sxs-lookup"><span data-stu-id="4c15d-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="4c15d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c15d-108">EXAMPLES</span></span>

### <span data-ttu-id="4c15d-109">Esempio 1: Impostare il tipo di protezione TDE (Transparent Data Encryption) su ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="4c15d-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="4c15d-110">Questo comando aggiorna il tipo di protezione TDE di un server a Service Managed.</span><span class="sxs-lookup"><span data-stu-id="4c15d-110">This command updates a server's TDE protector type to Service Managed.</span></span>
<span data-ttu-id="4c15d-111">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="4c15d-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="4c15d-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="4c15d-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="4c15d-113">Esempio 2: Impostare il tipo di protezione Crittografia dati trasparente su Vault chiave di Azure</span><span class="sxs-lookup"><span data-stu-id="4c15d-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="4c15d-114">Questo comando aggiorna un server in modo da usare la chiave del Vault della chiave del server con ID https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' ' come protezione TDE.</span><span class="sxs-lookup"><span data-stu-id="4c15d-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>
<span data-ttu-id="4c15d-115">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="4c15d-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="4c15d-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="4c15d-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="4c15d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c15d-117">PARAMETERS</span></span>

### <span data-ttu-id="4c15d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c15d-118">-AsJob</span></span>
<span data-ttu-id="4c15d-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4c15d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c15d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c15d-120">-DefaultProfile</span></span>
<span data-ttu-id="4c15d-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4c15d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c15d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="4c15d-122">-Force</span></span>
<span data-ttu-id="4c15d-123">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="4c15d-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="4c15d-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="4c15d-124">-KeyId</span></span>
<span data-ttu-id="4c15d-125">KeyId della chiave del Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c15d-125">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c15d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c15d-126">-ResourceGroupName</span></span>
<span data-ttu-id="4c15d-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4c15d-127">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c15d-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4c15d-128">-ServerName</span></span>
<span data-ttu-id="4c15d-129">Nome del server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c15d-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c15d-130">-Type</span><span class="sxs-lookup"><span data-stu-id="4c15d-130">-Type</span></span>
<span data-ttu-id="4c15d-131">Tipo di protezione TDE del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c15d-131">The Azure Sql Database TDE protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c15d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c15d-132">-Confirm</span></span>
<span data-ttu-id="4c15d-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c15d-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c15d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c15d-134">-WhatIf</span></span>
<span data-ttu-id="4c15d-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c15d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c15d-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c15d-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c15d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c15d-137">CommonParameters</span></span>
<span data-ttu-id="4c15d-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c15d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c15d-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4c15d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c15d-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="4c15d-140">INPUTS</span></span>

### <span data-ttu-id="4c15d-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="4c15d-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>

### <span data-ttu-id="4c15d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="4c15d-142">System.String</span></span>

## <span data-ttu-id="4c15d-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c15d-143">OUTPUTS</span></span>

### <span data-ttu-id="4c15d-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="4c15d-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="4c15d-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="4c15d-145">NOTES</span></span>

## <span data-ttu-id="4c15d-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c15d-146">RELATED LINKS</span></span>

[<span data-ttu-id="4c15d-147">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="4c15d-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
