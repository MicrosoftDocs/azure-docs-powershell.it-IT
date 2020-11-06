---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: f574e8e67f249ac1c7a4a3878ecc93a0a1eabc5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512159"
---
# <span data-ttu-id="1dc9a-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="1dc9a-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="1dc9a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1dc9a-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc9a-103">Imposta un criterio di Geo backup del database.</span><span class="sxs-lookup"><span data-stu-id="1dc9a-103">Sets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dc9a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1dc9a-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dc9a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1dc9a-105">DESCRIPTION</span></span>
<span data-ttu-id="1dc9a-106">Il cmdlet **set-AzureRmSqlDatabaseGeoBackupPolicy** imposta i criteri di backup Geo registrati in un database.</span><span class="sxs-lookup"><span data-stu-id="1dc9a-106">The **Set-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="1dc9a-107">Questa è una risorsa di backup di Azure usata per definire i criteri di archiviazione di backup.</span><span class="sxs-lookup"><span data-stu-id="1dc9a-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="1dc9a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1dc9a-108">EXAMPLES</span></span>

## <span data-ttu-id="1dc9a-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1dc9a-109">PARAMETERS</span></span>

### <span data-ttu-id="1dc9a-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1dc9a-110">-DatabaseName</span></span>
<span data-ttu-id="1dc9a-111">Specifica il nome del database per cui questo cmdlet imposta i criteri di backup Geo.</span><span class="sxs-lookup"><span data-stu-id="1dc9a-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="1dc9a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc9a-112">-DefaultProfile</span></span>
<span data-ttu-id="1dc9a-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1dc9a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dc9a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dc9a-114">-ResourceGroupName</span></span>
<span data-ttu-id="1dc9a-115">Specifica il nome del gruppo di risorse del server che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="1dc9a-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="1dc9a-116">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="1dc9a-116">-ServerName</span></span>
<span data-ttu-id="1dc9a-117">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="1dc9a-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="1dc9a-118">-Stato</span><span class="sxs-lookup"><span data-stu-id="1dc9a-118">-State</span></span>
<span data-ttu-id="1dc9a-119">Specifica lo stato dei criteri di backup Geo.</span><span class="sxs-lookup"><span data-stu-id="1dc9a-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="1dc9a-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1dc9a-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1dc9a-121">Abilitato</span><span class="sxs-lookup"><span data-stu-id="1dc9a-121">Enabled</span></span> 
- <span data-ttu-id="1dc9a-122">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="1dc9a-122">Disabled</span></span>

```yaml
Type: GeoBackupPolicyState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc9a-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1dc9a-123">-Confirm</span></span>
<span data-ttu-id="1dc9a-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dc9a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dc9a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dc9a-125">-WhatIf</span></span>
<span data-ttu-id="1dc9a-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dc9a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dc9a-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dc9a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dc9a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc9a-128">CommonParameters</span></span>
<span data-ttu-id="1dc9a-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dc9a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc9a-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dc9a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc9a-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1dc9a-131">INPUTS</span></span>

### <span data-ttu-id="1dc9a-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1dc9a-132">None</span></span>
<span data-ttu-id="1dc9a-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="1dc9a-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1dc9a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1dc9a-134">OUTPUTS</span></span>

## <span data-ttu-id="1dc9a-135">Note</span><span class="sxs-lookup"><span data-stu-id="1dc9a-135">NOTES</span></span>

## <span data-ttu-id="1dc9a-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1dc9a-136">RELATED LINKS</span></span>

[<span data-ttu-id="1dc9a-137">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="1dc9a-137">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="1dc9a-138">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="1dc9a-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

