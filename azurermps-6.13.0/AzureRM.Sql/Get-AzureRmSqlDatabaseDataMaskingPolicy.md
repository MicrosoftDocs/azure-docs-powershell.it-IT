---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 6b787e3347c20e011193d0b3968e036d53f62226
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518523"
---
# <span data-ttu-id="2ca49-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="2ca49-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="2ca49-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ca49-102">SYNOPSIS</span></span>
<span data-ttu-id="2ca49-103">Ottiene i criteri di mascheramento dei dati per un database.</span><span class="sxs-lookup"><span data-stu-id="2ca49-103">Gets the data masking policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ca49-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ca49-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ca49-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ca49-105">DESCRIPTION</span></span>
<span data-ttu-id="2ca49-106">Il cmdlet **Get-AzureRmSqlDatabaseDataMaskingPolicy** ottiene i criteri di mascheramento dei dati di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="2ca49-106">The **Get-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="2ca49-107">Per usare questo cmdlet, usare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="2ca49-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="2ca49-108">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="2ca49-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="2ca49-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ca49-109">EXAMPLES</span></span>

### <span data-ttu-id="2ca49-110">Esempio 1: ottenere i criteri di mascheramento dei dati per un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="2ca49-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="2ca49-111">Questo comando consente di ottenere i criteri di mascheramento dei dati da database Database01 nel gruppo di risorse ResourceGroup01 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="2ca49-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="2ca49-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ca49-112">PARAMETERS</span></span>

### <span data-ttu-id="2ca49-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2ca49-113">-DatabaseName</span></span>
<span data-ttu-id="2ca49-114">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="2ca49-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="2ca49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ca49-115">-DefaultProfile</span></span>
<span data-ttu-id="2ca49-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2ca49-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ca49-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ca49-117">-ResourceGroupName</span></span>
<span data-ttu-id="2ca49-118">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="2ca49-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="2ca49-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="2ca49-119">-ServerName</span></span>
<span data-ttu-id="2ca49-120">Specifica il nome del server in cui si trova il database.</span><span class="sxs-lookup"><span data-stu-id="2ca49-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="2ca49-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2ca49-121">-Confirm</span></span>
<span data-ttu-id="2ca49-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ca49-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ca49-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ca49-123">-WhatIf</span></span>
<span data-ttu-id="2ca49-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ca49-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ca49-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ca49-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ca49-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ca49-126">CommonParameters</span></span>
<span data-ttu-id="2ca49-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ca49-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ca49-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ca49-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ca49-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ca49-129">INPUTS</span></span>

### <span data-ttu-id="2ca49-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2ca49-130">System.String</span></span>

## <span data-ttu-id="2ca49-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ca49-131">OUTPUTS</span></span>

### <span data-ttu-id="2ca49-132">Microsoft. Azure. Commands. SQL. datamasking. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="2ca49-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="2ca49-133">Note</span><span class="sxs-lookup"><span data-stu-id="2ca49-133">NOTES</span></span>

## <span data-ttu-id="2ca49-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ca49-134">RELATED LINKS</span></span>

[<span data-ttu-id="2ca49-135">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2ca49-135">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2ca49-136">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2ca49-136">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2ca49-137">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2ca49-137">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2ca49-138">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="2ca49-138">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="2ca49-139">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2ca49-139">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)


