---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: b13a09a018ff85a48dd2baf3cf8837950a325cfc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688489"
---
# <span data-ttu-id="2f7cb-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="2f7cb-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="2f7cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2f7cb-102">SYNOPSIS</span></span>
<span data-ttu-id="2f7cb-103">Imposta la protezione per la crittografia dei dati trasparente (Transparent Data Encryption) per un server SQL.</span><span class="sxs-lookup"><span data-stu-id="2f7cb-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f7cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2f7cb-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f7cb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f7cb-105">DESCRIPTION</span></span>
<span data-ttu-id="2f7cb-106">Il cmdlet Set-AzureRmSqlServerTransparentDataEncryptionProtector imposta la protezione di Transparent per un server SQL.</span><span class="sxs-lookup"><span data-stu-id="2f7cb-106">The Set-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="2f7cb-107">La modifica del tipo di protezione di Transparent di transformazione ruota il Protector.</span><span class="sxs-lookup"><span data-stu-id="2f7cb-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="2f7cb-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2f7cb-108">EXAMPLES</span></span>

### <span data-ttu-id="2f7cb-109">--------------------------Esempio 1: impostare il tipo di protezione Transparent Data Encryption (ServiceManaged) su--------------------------</span><span class="sxs-lookup"><span data-stu-id="2f7cb-109">--------------------------  Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged  --------------------------</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="2f7cb-110">Questo comando Aggiorna il tipo di protezione transparent di un server a Service Managed.</span><span class="sxs-lookup"><span data-stu-id="2f7cb-110">This command updates a server's TDE protector type to Service Managed.</span></span>

<span data-ttu-id="2f7cb-111">ResourceGroupName nomeserver tipo ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="2f7cb-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="2f7cb-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="2f7cb-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="2f7cb-113">--------------------------Esempio 2: impostare il tipo di protezione di crittografia dati trasparente in Azure Key Vault--------------------------</span><span class="sxs-lookup"><span data-stu-id="2f7cb-113">--------------------------  Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault  --------------------------</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="2f7cb-114">Questo comando aggiorna un server in modo da usare la chiave del Vault del server Key con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' come protezione di Transcriptor.</span><span class="sxs-lookup"><span data-stu-id="2f7cb-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

<span data-ttu-id="2f7cb-115">ResourceGroupName nomeserver tipo ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="2f7cb-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="2f7cb-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="2f7cb-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="2f7cb-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2f7cb-117">PARAMETERS</span></span>

### <span data-ttu-id="2f7cb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2f7cb-118">-Force</span></span>
<span data-ttu-id="2f7cb-119">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="2f7cb-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="2f7cb-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="2f7cb-120">-KeyId</span></span>
<span data-ttu-id="2f7cb-121">Il Vault Key di Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="2f7cb-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="2f7cb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f7cb-122">-ResourceGroupName</span></span>
<span data-ttu-id="2f7cb-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2f7cb-123">The name of the resource group</span></span>

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

### <span data-ttu-id="2f7cb-124">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="2f7cb-124">-ServerName</span></span>
<span data-ttu-id="2f7cb-125">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2f7cb-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="2f7cb-126">-Digitare</span><span class="sxs-lookup"><span data-stu-id="2f7cb-126">-Type</span></span>
<span data-ttu-id="2f7cb-127">Tipo di protezione transparent di Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="2f7cb-127">The Azure Sql Database TDE protector type.</span></span>

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

### <span data-ttu-id="2f7cb-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2f7cb-128">-Confirm</span></span>
<span data-ttu-id="2f7cb-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f7cb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f7cb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f7cb-130">-WhatIf</span></span>
<span data-ttu-id="2f7cb-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2f7cb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f7cb-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2f7cb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f7cb-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f7cb-133">-DefaultProfile</span></span>
<span data-ttu-id="2f7cb-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2f7cb-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f7cb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f7cb-135">CommonParameters</span></span>
<span data-ttu-id="2f7cb-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f7cb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f7cb-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f7cb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f7cb-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2f7cb-138">INPUTS</span></span>

### <span data-ttu-id="2f7cb-139">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="2f7cb-139">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>
<span data-ttu-id="2f7cb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2f7cb-140">System.String</span></span>

## <span data-ttu-id="2f7cb-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2f7cb-141">OUTPUTS</span></span>

### <span data-ttu-id="2f7cb-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="2f7cb-142">System.Object</span></span>

## <span data-ttu-id="2f7cb-143">Note</span><span class="sxs-lookup"><span data-stu-id="2f7cb-143">NOTES</span></span>

## <span data-ttu-id="2f7cb-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2f7cb-144">RELATED LINKS</span></span>

[<span data-ttu-id="2f7cb-145">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="2f7cb-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
