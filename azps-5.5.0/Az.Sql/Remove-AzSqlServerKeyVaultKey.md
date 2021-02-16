---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 696f7bd0334039691301f8a4399362b9383ab2db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197654"
---
# <span data-ttu-id="5f6f6-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5f6f6-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="5f6f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f6f6-102">SYNOPSIS</span></span>
<span data-ttu-id="5f6f6-103">Rimuove una chiave del Vault chiave da un SQL server.</span><span class="sxs-lookup"><span data-stu-id="5f6f6-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="5f6f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f6f6-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f6f6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5f6f6-105">DESCRIPTION</span></span>
<span data-ttu-id="5f6f6-106">Il cmdlet Remove-AzSqlServerKeyVaultKey rimuove la chiave del Vault chiave dal server SQL specificato.</span><span class="sxs-lookup"><span data-stu-id="5f6f6-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="5f6f6-107">Si noti che SQL autorizzazioni del server di archiviazione della chiave per il vault della chiave non vengono modificate.</span><span class="sxs-lookup"><span data-stu-id="5f6f6-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="5f6f6-108">Per modificare le autorizzazioni, usare Set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="5f6f6-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="5f6f6-109">Si noti che questo cmdlet non apporta alcuna modifica al Vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="5f6f6-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="5f6f6-110">Per rimuovere una chiave dal Vault delle chiavi, usare Remove-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="5f6f6-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="5f6f6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f6f6-111">EXAMPLES</span></span>

### <span data-ttu-id="5f6f6-112">Esempio 1: Rimuovere una chiave del Vault chiave</span><span class="sxs-lookup"><span data-stu-id="5f6f6-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="5f6f6-113">Questo comando rimuove la chiave del Vault chiave con ID https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' ' dal server specificato.</span><span class="sxs-lookup"><span data-stu-id="5f6f6-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="5f6f6-114">ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Type : AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 112233445566778990011223344556677889900 CreationDate : 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="5f6f6-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="5f6f6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f6f6-115">PARAMETERS</span></span>

### <span data-ttu-id="5f6f6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f6f6-116">-AsJob</span></span>
<span data-ttu-id="5f6f6-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5f6f6-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5f6f6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f6f6-118">-DefaultProfile</span></span>
<span data-ttu-id="5f6f6-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="5f6f6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f6f6-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="5f6f6-120">-KeyId</span></span>
<span data-ttu-id="5f6f6-121">KeyId del Vault della chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="5f6f6-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="5f6f6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f6f6-122">-ResourceGroupName</span></span>
<span data-ttu-id="5f6f6-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="5f6f6-123">The name of the resource group</span></span>

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

### <span data-ttu-id="5f6f6-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5f6f6-124">-ServerName</span></span>
<span data-ttu-id="5f6f6-125">Nome del server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="5f6f6-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="5f6f6-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f6f6-126">-Confirm</span></span>
<span data-ttu-id="5f6f6-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f6f6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f6f6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f6f6-128">-WhatIf</span></span>
<span data-ttu-id="5f6f6-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f6f6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f6f6-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f6f6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f6f6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f6f6-131">CommonParameters</span></span>
<span data-ttu-id="5f6f6-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f6f6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f6f6-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5f6f6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f6f6-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="5f6f6-134">INPUTS</span></span>

### <span data-ttu-id="5f6f6-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5f6f6-135">System.String</span></span>

## <span data-ttu-id="5f6f6-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f6f6-136">OUTPUTS</span></span>

### <span data-ttu-id="5f6f6-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="5f6f6-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="5f6f6-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="5f6f6-138">NOTES</span></span>

## <span data-ttu-id="5f6f6-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f6f6-139">RELATED LINKS</span></span>

[<span data-ttu-id="5f6f6-140">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="5f6f6-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
