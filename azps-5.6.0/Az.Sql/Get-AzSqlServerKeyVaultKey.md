---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 523192b1632bf6ed67dff170b2ac94374c443299
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997301"
---
# <span data-ttu-id="e504d-101">Get-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e504d-101">Get-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="e504d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e504d-102">SYNOPSIS</span></span>
<span data-ttu-id="e504d-103">Ottiene le chiavi SQL Vault delle chiavi del server.</span><span class="sxs-lookup"><span data-stu-id="e504d-103">Gets a SQL server's Key Vault keys.</span></span>

## <span data-ttu-id="e504d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e504d-104">SYNTAX</span></span>

```
Get-AzSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e504d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e504d-105">DESCRIPTION</span></span>
<span data-ttu-id="e504d-106">Il cmdlet Get-AzSqlServerKeyVaultKey cmdlet ottiene informazioni sulle chiavi del Vault delle chiavi in un SQL server.</span><span class="sxs-lookup"><span data-stu-id="e504d-106">The Get-AzSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="e504d-107">È possibile visualizzare tutte le chiavi in un server o una chiave specifica fornendo il valore di KeyId.</span><span class="sxs-lookup"><span data-stu-id="e504d-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="e504d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e504d-108">EXAMPLES</span></span>

### <span data-ttu-id="e504d-109">Esempio 1: Ottenere tutte le chiavi del Vault chiave</span><span class="sxs-lookup"><span data-stu-id="e504d-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="e504d-110">Questo comando recupera tutte le chiavi del Vault delle chiavi in un SQL server.</span><span class="sxs-lookup"><span data-stu-id="e504d-110">This command gets all the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="e504d-111">ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Type : AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 112233445566778990011223344556677889900 CreationDate : 1/1/2017 12:00:00:00 AM ResourceDateGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey2_01234567890123456789012345678901 Type : AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint : 00998877665544322110099887665544332211 CreationDate : 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="e504d-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="e504d-112">Esempio 2: Ottenere una chiave specifica del Vault delle chiavi</span><span class="sxs-lookup"><span data-stu-id="e504d-112">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="e504d-113">Questo comando ottiene la chiave del Vault chiave con ID ' ' e quindi la archivia https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 nella variabile $MyServerKeyVaultKey chiave.</span><span class="sxs-lookup"><span data-stu-id="e504d-113">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="e504d-114">È possibile esaminare le proprietà dei $MyServerKeyVaultKey per ottenere informazioni dettagliate sul vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="e504d-114">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="e504d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e504d-115">PARAMETERS</span></span>

### <span data-ttu-id="e504d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e504d-116">-DefaultProfile</span></span>
<span data-ttu-id="e504d-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e504d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e504d-118">-KeyId</span><span class="sxs-lookup"><span data-stu-id="e504d-118">-KeyId</span></span>
<span data-ttu-id="e504d-119">KeyId della chiave del Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="e504d-119">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e504d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e504d-120">-ResourceGroupName</span></span>
<span data-ttu-id="e504d-121">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e504d-121">The name of the resource group</span></span>

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

### <span data-ttu-id="e504d-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e504d-122">-ServerName</span></span>
<span data-ttu-id="e504d-123">Nome del server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e504d-123">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="e504d-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e504d-124">-Confirm</span></span>
<span data-ttu-id="e504d-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e504d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e504d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e504d-126">-WhatIf</span></span>
<span data-ttu-id="e504d-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e504d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e504d-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e504d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e504d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e504d-129">CommonParameters</span></span>
<span data-ttu-id="e504d-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e504d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e504d-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e504d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e504d-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="e504d-132">INPUTS</span></span>

### <span data-ttu-id="e504d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e504d-133">System.String</span></span>

## <span data-ttu-id="e504d-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e504d-134">OUTPUTS</span></span>

### <span data-ttu-id="e504d-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="e504d-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="e504d-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="e504d-136">NOTES</span></span>

## <span data-ttu-id="e504d-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e504d-137">RELATED LINKS</span></span>

[<span data-ttu-id="e504d-138">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="e504d-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
