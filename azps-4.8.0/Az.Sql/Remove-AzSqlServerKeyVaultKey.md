---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 696f7bd0334039691301f8a4399362b9383ab2db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191856"
---
# <span data-ttu-id="046b0-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="046b0-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="046b0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="046b0-102">SYNOPSIS</span></span>
<span data-ttu-id="046b0-103">Rimuove una chiave di volta chiave da un server SQL.</span><span class="sxs-lookup"><span data-stu-id="046b0-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="046b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="046b0-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="046b0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="046b0-105">DESCRIPTION</span></span>
<span data-ttu-id="046b0-106">Il cmdlet Remove-AzSqlServerKeyVaultKey rimuove la chiave di volta chiave dal server SQL specificato.</span><span class="sxs-lookup"><span data-stu-id="046b0-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="046b0-107">Tieni presente che le autorizzazioni di SQL Server per il Vault della chiave non vengono modificate.</span><span class="sxs-lookup"><span data-stu-id="046b0-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="046b0-108">Per modificare le autorizzazioni, usare set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="046b0-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="046b0-109">Tieni presente che questo cmdlet non apporta alcuna modifica alla chiave Vault.</span><span class="sxs-lookup"><span data-stu-id="046b0-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="046b0-110">Per rimuovere una chiave da Vault chiave, usare Remove-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="046b0-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="046b0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="046b0-111">EXAMPLES</span></span>

### <span data-ttu-id="046b0-112">Esempio 1: rimuovere una chiave di volta chiave</span><span class="sxs-lookup"><span data-stu-id="046b0-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="046b0-113">Questo comando rimuove il Key Vault Key con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' dal server specificato.</span><span class="sxs-lookup"><span data-stu-id="046b0-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="046b0-114">ResourceGroupName: ContosoResourceGroup nomeserver: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 tipo: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 identificazione personale: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="046b0-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="046b0-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="046b0-115">PARAMETERS</span></span>

### <span data-ttu-id="046b0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="046b0-116">-AsJob</span></span>
<span data-ttu-id="046b0-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="046b0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="046b0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="046b0-118">-DefaultProfile</span></span>
<span data-ttu-id="046b0-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="046b0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="046b0-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="046b0-120">-KeyId</span></span>
<span data-ttu-id="046b0-121">Il Vault Key di Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="046b0-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="046b0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="046b0-122">-ResourceGroupName</span></span>
<span data-ttu-id="046b0-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="046b0-123">The name of the resource group</span></span>

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

### <span data-ttu-id="046b0-124">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="046b0-124">-ServerName</span></span>
<span data-ttu-id="046b0-125">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="046b0-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="046b0-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="046b0-126">-Confirm</span></span>
<span data-ttu-id="046b0-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="046b0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="046b0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="046b0-128">-WhatIf</span></span>
<span data-ttu-id="046b0-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="046b0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="046b0-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="046b0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="046b0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="046b0-131">CommonParameters</span></span>
<span data-ttu-id="046b0-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="046b0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="046b0-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="046b0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="046b0-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="046b0-134">INPUTS</span></span>

### <span data-ttu-id="046b0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="046b0-135">System.String</span></span>

## <span data-ttu-id="046b0-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="046b0-136">OUTPUTS</span></span>

### <span data-ttu-id="046b0-137">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="046b0-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="046b0-138">Note</span><span class="sxs-lookup"><span data-stu-id="046b0-138">NOTES</span></span>

## <span data-ttu-id="046b0-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="046b0-139">RELATED LINKS</span></span>

[<span data-ttu-id="046b0-140">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="046b0-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
