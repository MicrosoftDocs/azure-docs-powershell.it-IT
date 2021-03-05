---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: f354fe8ad1876eb756cdf78378dbf7048e53932d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961470"
---
# <span data-ttu-id="45ebd-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="45ebd-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="45ebd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="45ebd-103">Aggiunge una chiave del Vault chiave a un SQL server.</span><span class="sxs-lookup"><span data-stu-id="45ebd-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="45ebd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45ebd-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45ebd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="45ebd-105">DESCRIPTION</span></span>
<span data-ttu-id="45ebd-106">Il cmdlet Add-AzSqlServerKeyVaultKey aggiunge una chiave del Vault chiave al server SQL specificato.</span><span class="sxs-lookup"><span data-stu-id="45ebd-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="45ebd-107">Il server deve avere le autorizzazioni "get, wrapKey, unwrapKey" per il vault.</span><span class="sxs-lookup"><span data-stu-id="45ebd-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="45ebd-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45ebd-108">EXAMPLES</span></span>

### <span data-ttu-id="45ebd-109">Esempio 1: Aggiungere la chiave del Vault chiave</span><span class="sxs-lookup"><span data-stu-id="45ebd-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="45ebd-110">Questo comando aggiunge la chiave del Vault chiave con ID ' ' al server SQL denominato 'ContosoServer' nel gruppo di risorse https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 'ContosoResourceGroup'.</span><span class="sxs-lookup"><span data-stu-id="45ebd-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="45ebd-111">ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Type : AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 112233445566778990011223344556677889900 CreationDate : 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="45ebd-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="45ebd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45ebd-112">PARAMETERS</span></span>

### <span data-ttu-id="45ebd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45ebd-113">-AsJob</span></span>
<span data-ttu-id="45ebd-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="45ebd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45ebd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45ebd-115">-DefaultProfile</span></span>
<span data-ttu-id="45ebd-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="45ebd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45ebd-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="45ebd-117">-KeyId</span></span>
<span data-ttu-id="45ebd-118">KeyId del Vault della chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="45ebd-118">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45ebd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45ebd-119">-ResourceGroupName</span></span>
<span data-ttu-id="45ebd-120">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="45ebd-120">The name of the resource group</span></span>

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

### <span data-ttu-id="45ebd-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="45ebd-121">-ServerName</span></span>
<span data-ttu-id="45ebd-122">Nome del server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="45ebd-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="45ebd-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45ebd-123">-Confirm</span></span>
<span data-ttu-id="45ebd-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45ebd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45ebd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45ebd-125">-WhatIf</span></span>
<span data-ttu-id="45ebd-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45ebd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45ebd-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45ebd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45ebd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45ebd-128">CommonParameters</span></span>
<span data-ttu-id="45ebd-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45ebd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45ebd-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="45ebd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45ebd-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="45ebd-131">INPUTS</span></span>

### <span data-ttu-id="45ebd-132">System.String</span><span class="sxs-lookup"><span data-stu-id="45ebd-132">System.String</span></span>

## <span data-ttu-id="45ebd-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45ebd-133">OUTPUTS</span></span>

### <span data-ttu-id="45ebd-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="45ebd-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="45ebd-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="45ebd-135">NOTES</span></span>

## <span data-ttu-id="45ebd-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45ebd-136">RELATED LINKS</span></span>

[<span data-ttu-id="45ebd-137">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="45ebd-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
