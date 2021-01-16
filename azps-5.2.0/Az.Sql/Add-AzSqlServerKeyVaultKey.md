---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: f207726741155b22b16f8e69638c86eab684c658
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355495"
---
# <span data-ttu-id="246ea-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="246ea-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="246ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="246ea-102">SYNOPSIS</span></span>
<span data-ttu-id="246ea-103">Aggiunge una chiave di volta chiave a un server SQL.</span><span class="sxs-lookup"><span data-stu-id="246ea-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="246ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="246ea-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="246ea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="246ea-105">DESCRIPTION</span></span>
<span data-ttu-id="246ea-106">Il cmdlet Add-AzSqlServerKeyVaultKey aggiunge una chiave di volta chiave al server SQL fornito.</span><span class="sxs-lookup"><span data-stu-id="246ea-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="246ea-107">Il server deve avere le autorizzazioni ' Get, wrapKey, unwrapKey ' per il Vault.</span><span class="sxs-lookup"><span data-stu-id="246ea-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="246ea-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="246ea-108">EXAMPLES</span></span>

### <span data-ttu-id="246ea-109">Esempio 1: pulsante Aggiungi chiave volta</span><span class="sxs-lookup"><span data-stu-id="246ea-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="246ea-110">Questo comando aggiunge la chiave di volta chiave con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' a SQL Server denominato "ContosoServer" nel gruppo di risorse "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="246ea-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="246ea-111">ResourceGroupName: ContosoResourceGroup nomeserver: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 tipo: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 identificazione personale: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="246ea-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="246ea-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="246ea-112">PARAMETERS</span></span>

### <span data-ttu-id="246ea-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="246ea-113">-AsJob</span></span>
<span data-ttu-id="246ea-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="246ea-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="246ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="246ea-115">-DefaultProfile</span></span>
<span data-ttu-id="246ea-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="246ea-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="246ea-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="246ea-117">-KeyId</span></span>
<span data-ttu-id="246ea-118">Il Vault Key di Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="246ea-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="246ea-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="246ea-119">-ResourceGroupName</span></span>
<span data-ttu-id="246ea-120">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="246ea-120">The name of the resource group</span></span>

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

### <span data-ttu-id="246ea-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="246ea-121">-ServerName</span></span>
<span data-ttu-id="246ea-122">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="246ea-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="246ea-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="246ea-123">-Confirm</span></span>
<span data-ttu-id="246ea-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="246ea-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="246ea-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="246ea-125">-WhatIf</span></span>
<span data-ttu-id="246ea-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="246ea-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="246ea-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="246ea-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="246ea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="246ea-128">CommonParameters</span></span>
<span data-ttu-id="246ea-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="246ea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="246ea-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="246ea-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="246ea-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="246ea-131">INPUTS</span></span>

### <span data-ttu-id="246ea-132">System. String</span><span class="sxs-lookup"><span data-stu-id="246ea-132">System.String</span></span>

## <span data-ttu-id="246ea-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="246ea-133">OUTPUTS</span></span>

### <span data-ttu-id="246ea-134">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="246ea-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="246ea-135">Note</span><span class="sxs-lookup"><span data-stu-id="246ea-135">NOTES</span></span>

## <span data-ttu-id="246ea-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="246ea-136">RELATED LINKS</span></span>

[<span data-ttu-id="246ea-137">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="246ea-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
