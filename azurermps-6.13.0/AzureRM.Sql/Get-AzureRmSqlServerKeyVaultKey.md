---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 74d1909bee5eb4d2645fa1d25a429d1bc66d9f6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520606"
---
# <span data-ttu-id="856ac-101">Get-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="856ac-101">Get-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="856ac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="856ac-102">SYNOPSIS</span></span>
<span data-ttu-id="856ac-103">Ottiene le chiavi del Vault chiave di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="856ac-103">Gets a SQL server's Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="856ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="856ac-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="856ac-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="856ac-105">DESCRIPTION</span></span>
<span data-ttu-id="856ac-106">Il cmdlet Get-AzureRmSqlServerKeyVaultKey ottiene informazioni sulle chiavi del Vault chiave in un server SQL.</span><span class="sxs-lookup"><span data-stu-id="856ac-106">The Get-AzureRmSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="856ac-107">È possibile visualizzare tutti i tasti in un server o visualizzare un tasto specifico fornendo il KeyId.</span><span class="sxs-lookup"><span data-stu-id="856ac-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="856ac-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="856ac-108">EXAMPLES</span></span>

### <span data-ttu-id="856ac-109">Esempio 1: ottenere tutte le chiavi di volta chiave</span><span class="sxs-lookup"><span data-stu-id="856ac-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzureRmSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="856ac-110">Questo comando consente di ottenere tutte le chiavi del Vault chiave in un server SQL.</span><span class="sxs-lookup"><span data-stu-id="856ac-110">This command gets all the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="856ac-111">ResourceGroupName: ContosoResourceGroup nomeserver: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 tipo: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 identificazione personale: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM ResourceGroupName: ContosoResourceGroup nomeserver: ContosoServer ServerKeyName: Contoso_contosokey2_01234567890123456789012345678901 tipo: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 identificazione personale: 0099887766554433221100998877665544332211 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="856ac-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="856ac-112">Esempio 2: ottenere una chiave di volta chiave specifica</span><span class="sxs-lookup"><span data-stu-id="856ac-112">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="856ac-113">Questo comando ottiene la chiave di volta chiave con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' e lo archivia nella variabile $MyServerKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="856ac-113">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="856ac-114">Puoi ispezionare le proprietà di $MyServerKeyVaultKey per ottenere informazioni dettagliate sul Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="856ac-114">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="856ac-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="856ac-115">PARAMETERS</span></span>

### <span data-ttu-id="856ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="856ac-116">-DefaultProfile</span></span>
<span data-ttu-id="856ac-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="856ac-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="856ac-118">-KeyId</span><span class="sxs-lookup"><span data-stu-id="856ac-118">-KeyId</span></span>
<span data-ttu-id="856ac-119">Il Vault Key di Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="856ac-119">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="856ac-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="856ac-120">-ResourceGroupName</span></span>
<span data-ttu-id="856ac-121">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="856ac-121">The name of the resource group</span></span>

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

### <span data-ttu-id="856ac-122">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="856ac-122">-ServerName</span></span>
<span data-ttu-id="856ac-123">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="856ac-123">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="856ac-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="856ac-124">-Confirm</span></span>
<span data-ttu-id="856ac-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="856ac-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="856ac-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="856ac-126">-WhatIf</span></span>
<span data-ttu-id="856ac-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="856ac-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="856ac-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="856ac-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="856ac-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="856ac-129">CommonParameters</span></span>
<span data-ttu-id="856ac-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="856ac-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="856ac-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="856ac-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="856ac-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="856ac-132">INPUTS</span></span>

### <span data-ttu-id="856ac-133">System. String</span><span class="sxs-lookup"><span data-stu-id="856ac-133">System.String</span></span>

## <span data-ttu-id="856ac-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="856ac-134">OUTPUTS</span></span>

### <span data-ttu-id="856ac-135">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="856ac-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="856ac-136">Note</span><span class="sxs-lookup"><span data-stu-id="856ac-136">NOTES</span></span>

## <span data-ttu-id="856ac-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="856ac-137">RELATED LINKS</span></span>

[<span data-ttu-id="856ac-138">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="856ac-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
