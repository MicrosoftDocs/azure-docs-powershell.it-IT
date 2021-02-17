---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 951f1b6a03c621e0dd8bc5d559eaf317cfd43a2c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198878"
---
# <span data-ttu-id="16733-101">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="16733-101">Get-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="16733-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16733-102">SYNOPSIS</span></span>
<span data-ttu-id="16733-103">Ottenere tutte le sessioni di debug del flusso di dati attive da Data factory di Azure</span><span class="sxs-lookup"><span data-stu-id="16733-103">Get all active data flow debug sessions by Azure Data Factory</span></span>

## <span data-ttu-id="16733-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16733-104">SYNTAX</span></span>

### <span data-ttu-id="16733-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="16733-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16733-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="16733-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16733-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="16733-107">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16733-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="16733-108">DESCRIPTION</span></span>
<span data-ttu-id="16733-109">Elencare tutte le sessioni di debug del flusso di dati attive tramite Data factory di Azure con dettagli.</span><span class="sxs-lookup"><span data-stu-id="16733-109">List all active data flow debug sessions by Azure Data Factory with details.</span></span>

## <span data-ttu-id="16733-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16733-110">EXAMPLES</span></span>

### <span data-ttu-id="16733-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="16733-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Get-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF

SessionId                            ComputeType CoreCount                         StartTime                  LastActivityTime TimeToLiveInMinutes IntegrationRuntimeName                                      DataFlowName
---------                            ----------- ---------                         ---------                  ---------------- ------------------- ----------------------                                      ------------
3c68dbd6-f9c3-4b5f-a200-2310258016a7     General         8 2019-10-04T18:19:58.5550364+00:00 2019-10-04T18:24:51.3680548+00:00                  60                        DebugSession-0a7e0d6e-f2b7-48cc-8cd8-618326f5662f
```

<span data-ttu-id="16733-112">Ottenere tutte le sessioni di debug del flusso di dati attive in WikiADF di Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="16733-112">Get all active data flow debug sessions in Azure Data Factory "WikiADF".</span></span>

## <span data-ttu-id="16733-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16733-113">PARAMETERS</span></span>

### <span data-ttu-id="16733-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="16733-114">-DataFactory</span></span>
<span data-ttu-id="16733-115">Oggetto data factory.</span><span class="sxs-lookup"><span data-stu-id="16733-115">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16733-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="16733-116">-DataFactoryName</span></span>
<span data-ttu-id="16733-117">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="16733-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16733-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16733-118">-DefaultProfile</span></span>
<span data-ttu-id="16733-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16733-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16733-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16733-120">-ResourceGroupName</span></span>
<span data-ttu-id="16733-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="16733-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16733-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16733-122">-ResourceId</span></span>
<span data-ttu-id="16733-123">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="16733-123">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16733-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16733-124">CommonParameters</span></span>
<span data-ttu-id="16733-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16733-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16733-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="16733-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16733-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="16733-127">INPUTS</span></span>

### <span data-ttu-id="16733-128">System.String</span><span class="sxs-lookup"><span data-stu-id="16733-128">System.String</span></span>

### <span data-ttu-id="16733-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="16733-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="16733-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16733-130">OUTPUTS</span></span>

### <span data-ttu-id="16733-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowSessionInfo</span><span class="sxs-lookup"><span data-stu-id="16733-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span></span>

## <span data-ttu-id="16733-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="16733-132">NOTES</span></span>
<span data-ttu-id="16733-133">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="16733-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="16733-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16733-134">RELATED LINKS</span></span>

[<span data-ttu-id="16733-135">Start-AzDataSessionV2DataFlowFlowSession</span><span class="sxs-lookup"><span data-stu-id="16733-135">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="16733-136">Add-AzDataSessionV2DataFlowSessionPackage</span><span class="sxs-lookup"><span data-stu-id="16733-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="16733-137">Invoke-AzDataSessionV2DataFlowSessionCommand</span><span class="sxs-lookup"><span data-stu-id="16733-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="16733-138">Stop-AzDataSessionV2DataFlowFlowSession</span><span class="sxs-lookup"><span data-stu-id="16733-138">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)