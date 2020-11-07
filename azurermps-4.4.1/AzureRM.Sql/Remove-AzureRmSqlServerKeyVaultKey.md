---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: e8606f9eecfac63b68e9b8a26ecbebb89431e509
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685647"
---
# <span data-ttu-id="aac6a-101">Remove-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="aac6a-101">Remove-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="aac6a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aac6a-102">SYNOPSIS</span></span>
<span data-ttu-id="aac6a-103">Rimuove una chiave di volta chiave da un server SQL.</span><span class="sxs-lookup"><span data-stu-id="aac6a-103">Removes a Key Vault key from a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aac6a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aac6a-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aac6a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aac6a-105">DESCRIPTION</span></span>
<span data-ttu-id="aac6a-106">Il cmdlet Remove-AzureRmSqlServerKeyVaultKey rimuove la chiave di volta chiave dal server SQL specificato.</span><span class="sxs-lookup"><span data-stu-id="aac6a-106">The Remove-AzureRmSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>

<span data-ttu-id="aac6a-107">Tieni presente che le autorizzazioni di SQL Server per il Vault della chiave non vengono modificate.</span><span class="sxs-lookup"><span data-stu-id="aac6a-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="aac6a-108">Per modificare le autorizzazioni, usare set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="aac6a-108">To change permissions, use Set-AzureRmKeyVaultAccessPolicy.</span></span>

<span data-ttu-id="aac6a-109">Tieni presente che questo cmdlet non apporta alcuna modifica alla chiave Vault.</span><span class="sxs-lookup"><span data-stu-id="aac6a-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="aac6a-110">Per rimuovere una chiave da Vault chiave, usare Remove-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="aac6a-110">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="aac6a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aac6a-111">EXAMPLES</span></span>

### <span data-ttu-id="aac6a-112">--------------------------Esempio 1: rimuovere una chiave di volta chiave--------------------------</span><span class="sxs-lookup"><span data-stu-id="aac6a-112">--------------------------  Example 1: Remove a Key Vault key  --------------------------</span></span>
```
PS C:\> Remove-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="aac6a-113">Questo comando rimuove il Key Vault Key con ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' dal server specificato.</span><span class="sxs-lookup"><span data-stu-id="aac6a-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>

<span data-ttu-id="aac6a-114">ResourceGroupName: ContosoResourceGroup nomeserver: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 tipo: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 identificazione personale: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="aac6a-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="aac6a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aac6a-115">PARAMETERS</span></span>

### <span data-ttu-id="aac6a-116">-KeyId</span><span class="sxs-lookup"><span data-stu-id="aac6a-116">-KeyId</span></span>
<span data-ttu-id="aac6a-117">Il Vault Key di Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="aac6a-117">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="aac6a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aac6a-118">-ResourceGroupName</span></span>
<span data-ttu-id="aac6a-119">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="aac6a-119">The name of the resource group</span></span>

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

### <span data-ttu-id="aac6a-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="aac6a-120">-ServerName</span></span>
<span data-ttu-id="aac6a-121">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="aac6a-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="aac6a-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aac6a-122">-Confirm</span></span>
<span data-ttu-id="aac6a-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aac6a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aac6a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aac6a-124">-WhatIf</span></span>
<span data-ttu-id="aac6a-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aac6a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aac6a-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aac6a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aac6a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aac6a-127">-DefaultProfile</span></span>
<span data-ttu-id="aac6a-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aac6a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aac6a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac6a-129">CommonParameters</span></span>
<span data-ttu-id="aac6a-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aac6a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac6a-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aac6a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac6a-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aac6a-132">INPUTS</span></span>

### <span data-ttu-id="aac6a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="aac6a-133">System.String</span></span>

## <span data-ttu-id="aac6a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aac6a-134">OUTPUTS</span></span>

### <span data-ttu-id="aac6a-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="aac6a-135">System.Object</span></span>

## <span data-ttu-id="aac6a-136">Note</span><span class="sxs-lookup"><span data-stu-id="aac6a-136">NOTES</span></span>

## <span data-ttu-id="aac6a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aac6a-137">RELATED LINKS</span></span>

[<span data-ttu-id="aac6a-138">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="aac6a-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
