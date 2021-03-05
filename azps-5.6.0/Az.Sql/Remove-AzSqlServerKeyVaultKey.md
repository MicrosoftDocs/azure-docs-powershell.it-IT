---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 5b394909df0469c37a0217b3eb861ce4a1146e60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967342"
---
# <span data-ttu-id="eeb81-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="eeb81-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="eeb81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eeb81-102">SYNOPSIS</span></span>
<span data-ttu-id="eeb81-103">Rimuove una chiave del Vault chiave da un SQL server.</span><span class="sxs-lookup"><span data-stu-id="eeb81-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="eeb81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eeb81-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeb81-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eeb81-105">DESCRIPTION</span></span>
<span data-ttu-id="eeb81-106">Il cmdlet Remove-AzSqlServerKeyVaultKey rimuove la chiave del Vault chiave dal server SQL specificato.</span><span class="sxs-lookup"><span data-stu-id="eeb81-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="eeb81-107">Si noti che SQL le autorizzazioni del server della chiave per il vault della chiave non vengono modificate.</span><span class="sxs-lookup"><span data-stu-id="eeb81-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="eeb81-108">Per modificare le autorizzazioni, usare Set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="eeb81-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="eeb81-109">Si noti che questo cmdlet non apporta alcuna modifica al Vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="eeb81-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="eeb81-110">Per rimuovere una chiave dal Vault delle chiavi, usare Remove-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="eeb81-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="eeb81-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eeb81-111">EXAMPLES</span></span>

### <span data-ttu-id="eeb81-112">Esempio 1: Rimuovere una chiave del Vault chiave</span><span class="sxs-lookup"><span data-stu-id="eeb81-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="eeb81-113">Questo comando rimuove la chiave del Vault chiave con ID https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' ' dal server specificato.</span><span class="sxs-lookup"><span data-stu-id="eeb81-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="eeb81-114">ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Type : AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 112233445566778990011223344556677889900 CreationDate : 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="eeb81-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="eeb81-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eeb81-115">PARAMETERS</span></span>

### <span data-ttu-id="eeb81-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eeb81-116">-AsJob</span></span>
<span data-ttu-id="eeb81-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="eeb81-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eeb81-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeb81-118">-DefaultProfile</span></span>
<span data-ttu-id="eeb81-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="eeb81-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eeb81-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="eeb81-120">-KeyId</span></span>
<span data-ttu-id="eeb81-121">KeyId della chiave del Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="eeb81-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="eeb81-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeb81-122">-ResourceGroupName</span></span>
<span data-ttu-id="eeb81-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="eeb81-123">The name of the resource group</span></span>

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

### <span data-ttu-id="eeb81-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="eeb81-124">-ServerName</span></span>
<span data-ttu-id="eeb81-125">Nome del server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="eeb81-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="eeb81-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eeb81-126">-Confirm</span></span>
<span data-ttu-id="eeb81-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeb81-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeb81-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeb81-128">-WhatIf</span></span>
<span data-ttu-id="eeb81-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eeb81-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeb81-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eeb81-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeb81-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeb81-131">CommonParameters</span></span>
<span data-ttu-id="eeb81-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeb81-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeb81-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eeb81-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeb81-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="eeb81-134">INPUTS</span></span>

### <span data-ttu-id="eeb81-135">System.String</span><span class="sxs-lookup"><span data-stu-id="eeb81-135">System.String</span></span>

## <span data-ttu-id="eeb81-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eeb81-136">OUTPUTS</span></span>

### <span data-ttu-id="eeb81-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="eeb81-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="eeb81-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="eeb81-138">NOTES</span></span>

## <span data-ttu-id="eeb81-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eeb81-139">RELATED LINKS</span></span>

[<span data-ttu-id="eeb81-140">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="eeb81-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
