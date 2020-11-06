---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: a75ae79722fed99ce96b0a082f4f56ace998354e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510788"
---
# <span data-ttu-id="4ec70-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="4ec70-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="4ec70-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ec70-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec70-103">Sincronizza un database specificato nell'istanza specificata di Analysis Services server in tutte le istanze di scalabilità delle query nell'ambiente attualmente connesso, come specificato in comando Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4ec70-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ec70-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ec70-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ec70-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ec70-105">DESCRIPTION</span></span>
<span data-ttu-id="4ec70-106">Il cmdlet Sync-AzureAnalysisServicesInstance sincronizza un database specificato nell'istanza specificata di Analysis Services server per tutte le istanze di scalabilità delle query nell'ambiente attualmente connesso, come specificato in Add-AzureAnalysisServicesAccount comando</span><span class="sxs-lookup"><span data-stu-id="4ec70-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="4ec70-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ec70-107">EXAMPLES</span></span>

### <span data-ttu-id="4ec70-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4ec70-108">Example 1</span></span>
```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="4ec70-109">Questo comando Sincronizza il database denominato SalesOrders nel server denominato ' Contoso ' nell'ambiente westus.asazure.windows.net a condizione che l'utente abbia effettuato l'accesso a questo ambiente usando il comando Add-AzureAnalysisServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="4ec70-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="4ec70-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ec70-110">PARAMETERS</span></span>

### <span data-ttu-id="4ec70-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="4ec70-111">-Instance</span></span>
<span data-ttu-id="4ec70-112">Nome dell'istanza del server Analysis Services da riavviare</span><span class="sxs-lookup"><span data-stu-id="4ec70-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="4ec70-113">-Database</span><span class="sxs-lookup"><span data-stu-id="4ec70-113">-Database</span></span>
<span data-ttu-id="4ec70-114">Identità del database da sincronizzare</span><span class="sxs-lookup"><span data-stu-id="4ec70-114">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="4ec70-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ec70-115">-PassThru</span></span>
<span data-ttu-id="4ec70-116">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="4ec70-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="4ec70-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4ec70-117">-Confirm</span></span>
<span data-ttu-id="4ec70-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ec70-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ec70-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ec70-119">-WhatIf</span></span>
<span data-ttu-id="4ec70-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ec70-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ec70-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ec70-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ec70-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec70-122">CommonParameters</span></span>
<span data-ttu-id="4ec70-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ec70-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec70-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ec70-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec70-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ec70-125">INPUTS</span></span>

## <span data-ttu-id="4ec70-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ec70-126">OUTPUTS</span></span>

### <span data-ttu-id="4ec70-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4ec70-127">System.Boolean</span></span>

## <span data-ttu-id="4ec70-128">Note</span><span class="sxs-lookup"><span data-stu-id="4ec70-128">NOTES</span></span>
<span data-ttu-id="4ec70-129">Alias: Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="4ec70-129">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="4ec70-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ec70-130">RELATED LINKS</span></span>

