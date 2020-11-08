---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 696f7bd0334039691301f8a4399362b9383ab2db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021128"
---
# <span data-ttu-id="6ea87-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6ea87-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="6ea87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ea87-102">SYNOPSIS</span></span>
<span data-ttu-id="6ea87-103">Rimuove una chiave di volta chiave da un server SQL.</span><span class="sxs-lookup"><span data-stu-id="6ea87-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="6ea87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ea87-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ea87-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ea87-105">DESCRIPTION</span></span>
<span data-ttu-id="6ea87-106">Il cmdlet Remove-AzSqlServerKeyVaultKey rimuove la chiave di volta chiave dal server SQL specificato.</span><span class="sxs-lookup"><span data-stu-id="6ea87-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="6ea87-107">Tieni presente che le autorizzazioni di SQL Server per il Vault della chiave non vengono modificate.</span><span class="sxs-lookup"><span data-stu-id="6ea87-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="6ea87-108">Per modificare le autorizzazioni, usare set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="6ea87-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="6ea87-109">Tieni presente che questo cmdlet non apporta alcuna modifica alla chiave Vault.</span><span class="sxs-lookup"><span data-stu-id="6ea87-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="6ea87-110">Per rimuovere una chiave da Vault chiave, usare Remove-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="6ea87-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="6ea87-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ea87-111">EXAMPLES</span></span>

### <span data-ttu-id="6ea87-112">Esempio 1: rimuovere una chiave di volta chiave</span><span class="sxs-lookup"><span data-stu-id="6ea87-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="6ea87-113">Questo comando rimuove il Key Vault Key con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' dal server specificato.</span><span class="sxs-lookup"><span data-stu-id="6ea87-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="6ea87-114">ResourceGroupName: ContosoResourceGroup nomeserver: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 tipo: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 identificazione personale: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="6ea87-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="6ea87-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ea87-115">PARAMETERS</span></span>

### <span data-ttu-id="6ea87-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ea87-116">-AsJob</span></span>
<span data-ttu-id="6ea87-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6ea87-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ea87-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ea87-118">-DefaultProfile</span></span>
<span data-ttu-id="6ea87-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6ea87-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ea87-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="6ea87-120">-KeyId</span></span>
<span data-ttu-id="6ea87-121">Il Vault Key di Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="6ea87-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="6ea87-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ea87-122">-ResourceGroupName</span></span>
<span data-ttu-id="6ea87-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6ea87-123">The name of the resource group</span></span>

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

### <span data-ttu-id="6ea87-124">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="6ea87-124">-ServerName</span></span>
<span data-ttu-id="6ea87-125">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6ea87-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="6ea87-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6ea87-126">-Confirm</span></span>
<span data-ttu-id="6ea87-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ea87-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ea87-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ea87-128">-WhatIf</span></span>
<span data-ttu-id="6ea87-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ea87-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ea87-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ea87-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ea87-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ea87-131">CommonParameters</span></span>
<span data-ttu-id="6ea87-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ea87-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ea87-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ea87-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ea87-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ea87-134">INPUTS</span></span>

### <span data-ttu-id="6ea87-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6ea87-135">System.String</span></span>

## <span data-ttu-id="6ea87-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ea87-136">OUTPUTS</span></span>

### <span data-ttu-id="6ea87-137">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="6ea87-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="6ea87-138">Note</span><span class="sxs-lookup"><span data-stu-id="6ea87-138">NOTES</span></span>

## <span data-ttu-id="6ea87-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ea87-139">RELATED LINKS</span></span>

[<span data-ttu-id="6ea87-140">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="6ea87-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
