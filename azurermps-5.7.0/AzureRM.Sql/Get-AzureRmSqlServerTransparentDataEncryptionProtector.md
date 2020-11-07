---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: ecb49271c49e441140a43f8cb8ae5d65be56cd4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687414"
---
# <span data-ttu-id="6c041-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="6c041-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="6c041-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c041-102">SYNOPSIS</span></span>
<span data-ttu-id="6c041-103">Ottiene la protezione da crittografia dati trasparente (Transparent Data Encryption)</span><span class="sxs-lookup"><span data-stu-id="6c041-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c041-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c041-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c041-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c041-105">DESCRIPTION</span></span>
<span data-ttu-id="6c041-106">Il cmdlet Get-AzureRmSqlServerTransparentDataEncryptionProtector ottiene le informazioni relative al Protector di Transportation.</span><span class="sxs-lookup"><span data-stu-id="6c041-106">The Get-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="6c041-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c041-107">EXAMPLES</span></span>

### <span data-ttu-id="6c041-108">Esempio 1: ottenere la protezione da crittografia dati trasparente (Transparent Data Encryption)</span><span class="sxs-lookup"><span data-stu-id="6c041-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzureRmSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="6c041-109">Questo comando consente di ottenere la protezione di Transparent per il server denominato ContosoServer nel gruppo di risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6c041-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>

<span data-ttu-id="6c041-110">ResourceGroupName nomeserver tipo ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="6c041-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="6c041-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="6c041-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="6c041-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c041-112">PARAMETERS</span></span>

### <span data-ttu-id="6c041-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c041-113">-DefaultProfile</span></span>
<span data-ttu-id="6c041-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6c041-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c041-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c041-115">-ResourceGroupName</span></span>
<span data-ttu-id="6c041-116">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6c041-116">The name of the resource group</span></span>

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

### <span data-ttu-id="6c041-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="6c041-117">-ServerName</span></span>
<span data-ttu-id="6c041-118">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6c041-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="6c041-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6c041-119">-Confirm</span></span>
<span data-ttu-id="6c041-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c041-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c041-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c041-121">-WhatIf</span></span>
<span data-ttu-id="6c041-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c041-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c041-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c041-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c041-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c041-124">CommonParameters</span></span>
<span data-ttu-id="6c041-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c041-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c041-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c041-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c041-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c041-127">INPUTS</span></span>

### <span data-ttu-id="6c041-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6c041-128">System.String</span></span>

## <span data-ttu-id="6c041-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c041-129">OUTPUTS</span></span>

### <span data-ttu-id="6c041-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="6c041-130">System.Object</span></span>

## <span data-ttu-id="6c041-131">Note</span><span class="sxs-lookup"><span data-stu-id="6c041-131">NOTES</span></span>

## <span data-ttu-id="6c041-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c041-132">RELATED LINKS</span></span>

[<span data-ttu-id="6c041-133">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="6c041-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
