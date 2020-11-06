---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 732eb92a46fa7e69ba5274398de648c16142ae75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509499"
---
# <span data-ttu-id="f9458-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="f9458-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="f9458-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f9458-102">SYNOPSIS</span></span>

<span data-ttu-id="f9458-103">Sincronizza un database specificato nell'istanza specificata di Analysis Services server in tutte le istanze di scalabilità delle query nell'ambiente attualmente connesso, come specificato in comando Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f9458-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9458-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9458-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9458-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9458-105">DESCRIPTION</span></span>

<span data-ttu-id="f9458-106">Il cmdlet Sync-AzureAnalysisServicesInstance sincronizza un database specificato nell'istanza specificata di Analysis Services server per tutte le istanze di scalabilità delle query nell'ambiente attualmente connesso, come specificato in Add-AzureAnalysisServicesAccount comando</span><span class="sxs-lookup"><span data-stu-id="f9458-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="f9458-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9458-107">EXAMPLES</span></span>

### <span data-ttu-id="f9458-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f9458-108">Example 1</span></span>

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="f9458-109">Questo comando Sincronizza il database denominato SalesOrders nel server denominato ' Contoso ' nell'ambiente westus.asazure.windows.net a condizione che l'utente abbia effettuato l'accesso a questo ambiente usando il comando Add-AzureAnalysisServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="f9458-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="f9458-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f9458-110">PARAMETERS</span></span>

### <span data-ttu-id="f9458-111">-Database</span><span class="sxs-lookup"><span data-stu-id="f9458-111">-Database</span></span>

<span data-ttu-id="f9458-112">Identità del database da sincronizzare</span><span class="sxs-lookup"><span data-stu-id="f9458-112">Identity of the database to be synchronized</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9458-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="f9458-113">-Instance</span></span>

<span data-ttu-id="f9458-114">Nome dell'istanza del server Analysis Services da riavviare</span><span class="sxs-lookup"><span data-stu-id="f9458-114">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9458-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9458-115">-PassThru</span></span>

<span data-ttu-id="f9458-116">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="f9458-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f9458-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f9458-117">-Confirm</span></span>
<span data-ttu-id="f9458-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9458-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9458-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9458-119">-WhatIf</span></span>
<span data-ttu-id="f9458-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9458-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9458-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9458-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9458-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9458-122">CommonParameters</span></span>
<span data-ttu-id="f9458-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9458-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9458-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9458-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9458-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f9458-125">INPUTS</span></span>

### <span data-ttu-id="f9458-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f9458-126">System.String</span></span>
<span data-ttu-id="f9458-127">Parameters: database (ByValue), instance (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f9458-127">Parameters: Database (ByValue), Instance (ByValue)</span></span>

## <span data-ttu-id="f9458-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9458-128">OUTPUTS</span></span>

### <span data-ttu-id="f9458-129">Microsoft. Azure. Commands. AnalysisServices. dataplane. Models. ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="f9458-129">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="f9458-130">Note</span><span class="sxs-lookup"><span data-stu-id="f9458-130">NOTES</span></span>

<span data-ttu-id="f9458-131">Alias: Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="f9458-131">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="f9458-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9458-132">RELATED LINKS</span></span>
