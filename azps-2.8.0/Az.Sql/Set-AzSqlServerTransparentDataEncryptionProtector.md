---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: d2d2bd98491b5bf91aebb45e6b8a3368a58d1b56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857609"
---
# <span data-ttu-id="231d7-101">Set-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="231d7-101">Set-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="231d7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="231d7-102">SYNOPSIS</span></span>
<span data-ttu-id="231d7-103">Imposta la protezione per la crittografia dei dati trasparente (Transparent Data Encryption) per un server SQL.</span><span class="sxs-lookup"><span data-stu-id="231d7-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

## <span data-ttu-id="231d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="231d7-104">SYNTAX</span></span>

```
Set-AzSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="231d7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="231d7-105">DESCRIPTION</span></span>
<span data-ttu-id="231d7-106">Il cmdlet Set-AzSqlServerTransparentDataEncryptionProtector imposta la protezione di Transparent per un server SQL.</span><span class="sxs-lookup"><span data-stu-id="231d7-106">The Set-AzSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="231d7-107">La modifica del tipo di protezione di Transparent di transformazione ruota il Protector.</span><span class="sxs-lookup"><span data-stu-id="231d7-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="231d7-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="231d7-108">EXAMPLES</span></span>

### <span data-ttu-id="231d7-109">Esempio 1: impostare il tipo di protezione Transparent Data Encryption (ServiceManaged)</span><span class="sxs-lookup"><span data-stu-id="231d7-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="231d7-110">Questo comando Aggiorna il tipo di protezione transparent di un server a Service Managed.</span><span class="sxs-lookup"><span data-stu-id="231d7-110">This command updates a server's TDE protector type to Service Managed.</span></span>
<span data-ttu-id="231d7-111">ResourceGroupName nomeserver tipo ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="231d7-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="231d7-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="231d7-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="231d7-113">Esempio 2: impostare il tipo di protezione di crittografia dati trasparente in Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="231d7-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="231d7-114">Questo comando aggiorna un server in modo da usare la chiave del Vault del server Key con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' come protezione di Transcriptor.</span><span class="sxs-lookup"><span data-stu-id="231d7-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>
<span data-ttu-id="231d7-115">ResourceGroupName nomeserver tipo ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="231d7-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="231d7-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="231d7-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="231d7-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="231d7-117">PARAMETERS</span></span>

### <span data-ttu-id="231d7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="231d7-118">-AsJob</span></span>
<span data-ttu-id="231d7-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="231d7-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="231d7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="231d7-120">-DefaultProfile</span></span>
<span data-ttu-id="231d7-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="231d7-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="231d7-122">-Force</span><span class="sxs-lookup"><span data-stu-id="231d7-122">-Force</span></span>
<span data-ttu-id="231d7-123">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="231d7-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="231d7-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="231d7-124">-KeyId</span></span>
<span data-ttu-id="231d7-125">Il Vault Key di Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="231d7-125">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="231d7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="231d7-126">-ResourceGroupName</span></span>
<span data-ttu-id="231d7-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="231d7-127">The name of the resource group</span></span>

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

### <span data-ttu-id="231d7-128">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="231d7-128">-ServerName</span></span>
<span data-ttu-id="231d7-129">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="231d7-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="231d7-130">-Digitare</span><span class="sxs-lookup"><span data-stu-id="231d7-130">-Type</span></span>
<span data-ttu-id="231d7-131">Tipo di protezione transparent di Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="231d7-131">The Azure Sql Database TDE protector type.</span></span>

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

### <span data-ttu-id="231d7-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="231d7-132">-Confirm</span></span>
<span data-ttu-id="231d7-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="231d7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="231d7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="231d7-134">-WhatIf</span></span>
<span data-ttu-id="231d7-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="231d7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="231d7-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="231d7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="231d7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="231d7-137">CommonParameters</span></span>
<span data-ttu-id="231d7-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="231d7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="231d7-139">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="231d7-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="231d7-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="231d7-140">INPUTS</span></span>

### <span data-ttu-id="231d7-141">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="231d7-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>

### <span data-ttu-id="231d7-142">System. String</span><span class="sxs-lookup"><span data-stu-id="231d7-142">System.String</span></span>

## <span data-ttu-id="231d7-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="231d7-143">OUTPUTS</span></span>

### <span data-ttu-id="231d7-144">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="231d7-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="231d7-145">Note</span><span class="sxs-lookup"><span data-stu-id="231d7-145">NOTES</span></span>

## <span data-ttu-id="231d7-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="231d7-146">RELATED LINKS</span></span>

[<span data-ttu-id="231d7-147">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="231d7-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
