---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 333e4b1e5f01c76947ca32277fd8ca7ff75218eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685809"
---
# <span data-ttu-id="724b7-101">Remove-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="724b7-101">Remove-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="724b7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="724b7-102">SYNOPSIS</span></span>
<span data-ttu-id="724b7-103">Rimuove una chiave di volta chiave da un server SQL.</span><span class="sxs-lookup"><span data-stu-id="724b7-103">Removes a Key Vault key from a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="724b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="724b7-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="724b7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="724b7-105">DESCRIPTION</span></span>
<span data-ttu-id="724b7-106">Il cmdlet Remove-AzureRmSqlServerKeyVaultKey rimuove la chiave di volta chiave dal server SQL specificato.</span><span class="sxs-lookup"><span data-stu-id="724b7-106">The Remove-AzureRmSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>

<span data-ttu-id="724b7-107">Tieni presente che le autorizzazioni di SQL Server per il Vault della chiave non vengono modificate.</span><span class="sxs-lookup"><span data-stu-id="724b7-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="724b7-108">Per modificare le autorizzazioni, usare set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="724b7-108">To change permissions, use Set-AzureRmKeyVaultAccessPolicy.</span></span>

<span data-ttu-id="724b7-109">Tieni presente che questo cmdlet non apporta alcuna modifica alla chiave Vault.</span><span class="sxs-lookup"><span data-stu-id="724b7-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="724b7-110">Per rimuovere una chiave da Vault chiave, usare Remove-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="724b7-110">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="724b7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="724b7-111">EXAMPLES</span></span>

### <span data-ttu-id="724b7-112">Esempio 1: rimuovere una chiave di volta chiave</span><span class="sxs-lookup"><span data-stu-id="724b7-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="724b7-113">Questo comando rimuove il Key Vault Key con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' dal server specificato.</span><span class="sxs-lookup"><span data-stu-id="724b7-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>

<span data-ttu-id="724b7-114">ResourceGroupName: ContosoResourceGroup nomeserver: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 tipo: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 identificazione personale: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="724b7-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="724b7-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="724b7-115">PARAMETERS</span></span>

### <span data-ttu-id="724b7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="724b7-116">-AsJob</span></span>
<span data-ttu-id="724b7-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="724b7-117">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="724b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="724b7-118">-DefaultProfile</span></span>
<span data-ttu-id="724b7-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="724b7-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="724b7-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="724b7-120">-KeyId</span></span>
<span data-ttu-id="724b7-121">Il Vault Key di Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="724b7-121">The Azure Key Vault KeyId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="724b7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="724b7-122">-ResourceGroupName</span></span>
<span data-ttu-id="724b7-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="724b7-123">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="724b7-124">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="724b7-124">-ServerName</span></span>
<span data-ttu-id="724b7-125">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="724b7-125">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="724b7-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="724b7-126">-Confirm</span></span>
<span data-ttu-id="724b7-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="724b7-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="724b7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="724b7-128">-WhatIf</span></span>
<span data-ttu-id="724b7-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="724b7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="724b7-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="724b7-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="724b7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="724b7-131">CommonParameters</span></span>
<span data-ttu-id="724b7-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="724b7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="724b7-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="724b7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="724b7-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="724b7-134">INPUTS</span></span>

### <span data-ttu-id="724b7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="724b7-135">System.String</span></span>

## <span data-ttu-id="724b7-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="724b7-136">OUTPUTS</span></span>

### <span data-ttu-id="724b7-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="724b7-137">System.Object</span></span>

## <span data-ttu-id="724b7-138">Note</span><span class="sxs-lookup"><span data-stu-id="724b7-138">NOTES</span></span>

## <span data-ttu-id="724b7-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="724b7-139">RELATED LINKS</span></span>

[<span data-ttu-id="724b7-140">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="724b7-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
