---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlCapability.md
ms.openlocfilehash: 7d62a005455394dd1b00309adcf47bc639551a4e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514084"
---
# <span data-ttu-id="72479-101">Get-AzureRmSqlCapability</span><span class="sxs-lookup"><span data-stu-id="72479-101">Get-AzureRmSqlCapability</span></span>

## <span data-ttu-id="72479-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72479-102">SYNOPSIS</span></span>
<span data-ttu-id="72479-103">Ottiene le funzionalità di database SQL per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="72479-103">Gets SQL Database capabilities for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72479-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72479-104">SYNTAX</span></span>

### <span data-ttu-id="72479-105">FilterResults (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72479-105">FilterResults (Default)</span></span>
```
Get-AzureRmSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72479-106">DefaultResults</span><span class="sxs-lookup"><span data-stu-id="72479-106">DefaultResults</span></span>
```
Get-AzureRmSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72479-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72479-107">DESCRIPTION</span></span>
<span data-ttu-id="72479-108">Il cmdlet **Get-AzureRmSqlCapability** ottiene le funzionalità di database SQL di Azure disponibili nell'abbonamento corrente per un'area geografica.</span><span class="sxs-lookup"><span data-stu-id="72479-108">The **Get-AzureRmSqlCapability** cmdlet gets the Azure SQL Database capabilities available on the current subscription for a region.</span></span>
<span data-ttu-id="72479-109">Se specifichi i parametri *ServerVersionName* , *EditionName* o *ServiceObjectiveName* , questo cmdlet restituisce i valori specificati e i relativi predecessori.</span><span class="sxs-lookup"><span data-stu-id="72479-109">If you specify the *ServerVersionName* , *EditionName* , or *ServiceObjectiveName* parameters, this cmdlet returns the specified values and their predecessors.</span></span>

## <span data-ttu-id="72479-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72479-110">EXAMPLES</span></span>

### <span data-ttu-id="72479-111">Esempio 1: ottenere funzionalità per l'abbonamento corrente per un'area geografica</span><span class="sxs-lookup"><span data-stu-id="72479-111">Example 1: Get capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzureRmSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

<span data-ttu-id="72479-112">Questo comando restituisce le funzionalità per le istanze di database SQL nell'abbonamento corrente per l'area centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="72479-112">This command returns the capabilities for SQL Database instances on the current subscription for the Central US region.</span></span>

### <span data-ttu-id="72479-113">Esempio 2: ottenere funzionalità predefinite per l'abbonamento corrente per un'area geografica</span><span class="sxs-lookup"><span data-stu-id="72479-113">Example 2: Get default capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzureRmSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

<span data-ttu-id="72479-114">Questo comando restituisce le funzionalità predefinite per i database SQL nella sottoscrizione corrente nell'area centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="72479-114">This command returns the default capabilities for SQL Databases on the current subscription in the Central US region.</span></span>

### <span data-ttu-id="72479-115">Esempio 3: ottenere informazioni dettagliate per un obiettivo di servizio</span><span class="sxs-lookup"><span data-stu-id="72479-115">Example 3: Get details for a service objective</span></span>
```
PS C:\>Get-AzureRmSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

<span data-ttu-id="72479-116">Questo comando ottiene le funzionalità predefinite per i database SQL per l'obiettivo di servizio specificato nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="72479-116">This command gets default capabilities for SQL Databases for the specified service objective on the current subscription.</span></span>

## <span data-ttu-id="72479-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72479-117">PARAMETERS</span></span>

### <span data-ttu-id="72479-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72479-118">-DefaultProfile</span></span>
<span data-ttu-id="72479-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="72479-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72479-120">-Impostazioni predefinite</span><span class="sxs-lookup"><span data-stu-id="72479-120">-Defaults</span></span>
<span data-ttu-id="72479-121">Indica che questo cmdlet ottiene solo le impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="72479-121">Indicates that this cmdlet gets only defaults.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72479-122">-EditionName</span><span class="sxs-lookup"><span data-stu-id="72479-122">-EditionName</span></span>
<span data-ttu-id="72479-123">Specifica il nome dell'edizione del database per cui questo cmdlet ottiene le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="72479-123">Specifies the name of the database edition for which this cmdlet gets capabilities.</span></span>

```yaml
Type: String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72479-124">-LocationName</span><span class="sxs-lookup"><span data-stu-id="72479-124">-LocationName</span></span>
<span data-ttu-id="72479-125">Specifica il nome della posizione per cui questo cmdlet ottiene le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="72479-125">Specifies the name of the Location for which this cmdlet gets capabilities.</span></span>
<span data-ttu-id="72479-126">Per altre informazioni, vedere aree di Azure https://azure.microsoft.com/en-us/regions/ ( https://azure.microsoft.com/en-us/regions/) .</span><span class="sxs-lookup"><span data-stu-id="72479-126">For more information, see Azure Regionshttps://azure.microsoft.com/en-us/regions/ (https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="72479-127">-ServerVersionName</span><span class="sxs-lookup"><span data-stu-id="72479-127">-ServerVersionName</span></span>
<span data-ttu-id="72479-128">Specifica il nome della versione del server per cui questo cmdlet ottiene le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="72479-128">Specifies the name of the server version for which this cmdlet gets capabilities.</span></span>

```yaml
Type: String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72479-129">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="72479-129">-ServiceObjectiveName</span></span>
<span data-ttu-id="72479-130">Specifica il nome dell'obiettivo del servizio per cui questo cmdlet ottiene le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="72479-130">Specifies the name of the service objective for which this cmdlet gets capabilities.</span></span>

```yaml
Type: String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72479-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="72479-131">-Confirm</span></span>
<span data-ttu-id="72479-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72479-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72479-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72479-133">-WhatIf</span></span>
<span data-ttu-id="72479-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72479-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72479-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72479-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72479-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72479-136">CommonParameters</span></span>
<span data-ttu-id="72479-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72479-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72479-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72479-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72479-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72479-139">INPUTS</span></span>

### <span data-ttu-id="72479-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="72479-140">None</span></span>
<span data-ttu-id="72479-141">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="72479-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72479-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72479-142">OUTPUTS</span></span>

### <span data-ttu-id="72479-143">Microsoft.Azure.Commands.Sql.Location_Capabilities. Model. LocationCapabilityModel</span><span class="sxs-lookup"><span data-stu-id="72479-143">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span></span>

## <span data-ttu-id="72479-144">Note</span><span class="sxs-lookup"><span data-stu-id="72479-144">NOTES</span></span>

## <span data-ttu-id="72479-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72479-145">RELATED LINKS</span></span>