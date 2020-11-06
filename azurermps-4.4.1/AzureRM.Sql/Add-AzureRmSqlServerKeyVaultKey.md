---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: b9051f8729ae1cee8216de5d2dab6d5ceb79a717
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521518"
---
# <span data-ttu-id="ae628-101">Add-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ae628-101">Add-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="ae628-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae628-102">SYNOPSIS</span></span>
<span data-ttu-id="ae628-103">Aggiunge una chiave di volta chiave a un server SQL.</span><span class="sxs-lookup"><span data-stu-id="ae628-103">Adds a Key Vault key to a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae628-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae628-104">SYNTAX</span></span>

```
Add-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae628-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae628-105">DESCRIPTION</span></span>
<span data-ttu-id="ae628-106">Il cmdlet Add-AzureRmSqlServerKeyVaultKey aggiunge una chiave di volta chiave al server SQL fornito.</span><span class="sxs-lookup"><span data-stu-id="ae628-106">The Add-AzureRmSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="ae628-107">Il server deve avere le autorizzazioni ' Get, wrapKey, unwrapKey ' per il Vault.</span><span class="sxs-lookup"><span data-stu-id="ae628-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="ae628-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae628-108">EXAMPLES</span></span>

### <span data-ttu-id="ae628-109">--------------------------Esempio 1: aggiungere chiave di volta chiave--------------------------</span><span class="sxs-lookup"><span data-stu-id="ae628-109">--------------------------  Example 1: Add Key Vault key  --------------------------</span></span>
```
PS C:\> Add-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="ae628-110">Questo comando aggiunge la chiave di volta chiave con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' a SQL Server denominato "ContosoServer" nel gruppo di risorse "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="ae628-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>

<span data-ttu-id="ae628-111">ResourceGroupName: ContosoResourceGroup nomeserver: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 tipo: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 identificazione personale: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="ae628-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="ae628-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae628-112">PARAMETERS</span></span>

### <span data-ttu-id="ae628-113">-KeyId</span><span class="sxs-lookup"><span data-stu-id="ae628-113">-KeyId</span></span>
<span data-ttu-id="ae628-114">Il Vault Key di Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="ae628-114">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="ae628-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae628-115">-ResourceGroupName</span></span>
<span data-ttu-id="ae628-116">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ae628-116">The name of the resource group</span></span>

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

### <span data-ttu-id="ae628-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="ae628-117">-ServerName</span></span>
<span data-ttu-id="ae628-118">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ae628-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="ae628-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ae628-119">-Confirm</span></span>
<span data-ttu-id="ae628-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae628-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae628-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae628-121">-WhatIf</span></span>
<span data-ttu-id="ae628-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae628-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae628-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae628-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae628-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae628-124">-DefaultProfile</span></span>
<span data-ttu-id="ae628-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae628-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae628-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae628-126">CommonParameters</span></span>
<span data-ttu-id="ae628-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae628-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae628-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae628-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae628-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae628-129">INPUTS</span></span>

### <span data-ttu-id="ae628-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ae628-130">System.String</span></span>

## <span data-ttu-id="ae628-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae628-131">OUTPUTS</span></span>

### <span data-ttu-id="ae628-132">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="ae628-132">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="ae628-133">Note</span><span class="sxs-lookup"><span data-stu-id="ae628-133">NOTES</span></span>

## <span data-ttu-id="ae628-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae628-134">RELATED LINKS</span></span>

[<span data-ttu-id="ae628-135">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="ae628-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
