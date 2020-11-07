---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 9b07a7d9113411b83c97818d6d34c5a7df40c8fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677038"
---
# <span data-ttu-id="2449e-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2449e-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="2449e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2449e-102">SYNOPSIS</span></span>
<span data-ttu-id="2449e-103">Aggiunge una chiave di volta chiave a un server SQL.</span><span class="sxs-lookup"><span data-stu-id="2449e-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="2449e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2449e-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2449e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2449e-105">DESCRIPTION</span></span>
<span data-ttu-id="2449e-106">Il cmdlet Add-AzSqlServerKeyVaultKey aggiunge una chiave di volta chiave al server SQL fornito.</span><span class="sxs-lookup"><span data-stu-id="2449e-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="2449e-107">Il server deve avere le autorizzazioni ' Get, wrapKey, unwrapKey ' per il Vault.</span><span class="sxs-lookup"><span data-stu-id="2449e-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="2449e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2449e-108">EXAMPLES</span></span>

### <span data-ttu-id="2449e-109">Esempio 1: pulsante Aggiungi chiave volta</span><span class="sxs-lookup"><span data-stu-id="2449e-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="2449e-110">Questo comando aggiunge la chiave di volta chiave con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' a SQL Server denominato "ContosoServer" nel gruppo di risorse "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="2449e-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="2449e-111">ResourceGroupName: ContosoResourceGroup nomeserver: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 tipo: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 identificazione personale: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="2449e-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="2449e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2449e-112">PARAMETERS</span></span>

### <span data-ttu-id="2449e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2449e-113">-AsJob</span></span>
<span data-ttu-id="2449e-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2449e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2449e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2449e-115">-DefaultProfile</span></span>
<span data-ttu-id="2449e-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2449e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2449e-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="2449e-117">-KeyId</span></span>
<span data-ttu-id="2449e-118">Il Vault Key di Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="2449e-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="2449e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2449e-119">-ResourceGroupName</span></span>
<span data-ttu-id="2449e-120">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2449e-120">The name of the resource group</span></span>

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

### <span data-ttu-id="2449e-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="2449e-121">-ServerName</span></span>
<span data-ttu-id="2449e-122">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2449e-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="2449e-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2449e-123">-Confirm</span></span>
<span data-ttu-id="2449e-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2449e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2449e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2449e-125">-WhatIf</span></span>
<span data-ttu-id="2449e-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2449e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2449e-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2449e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2449e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2449e-128">CommonParameters</span></span>
<span data-ttu-id="2449e-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2449e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2449e-130">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2449e-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2449e-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2449e-131">INPUTS</span></span>

### <span data-ttu-id="2449e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2449e-132">System.String</span></span>

## <span data-ttu-id="2449e-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2449e-133">OUTPUTS</span></span>

### <span data-ttu-id="2449e-134">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="2449e-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="2449e-135">Note</span><span class="sxs-lookup"><span data-stu-id="2449e-135">NOTES</span></span>

## <span data-ttu-id="2449e-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2449e-136">RELATED LINKS</span></span>

[<span data-ttu-id="2449e-137">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="2449e-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)