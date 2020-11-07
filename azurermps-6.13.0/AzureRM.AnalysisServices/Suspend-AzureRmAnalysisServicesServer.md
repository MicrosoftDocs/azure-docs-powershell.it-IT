---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/suspend-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 0fc666ef1b747c7c114de560d241bcc2ac7be1f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686979"
---
# <span data-ttu-id="667a6-101">Suspend-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="667a6-101">Suspend-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="667a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="667a6-102">SYNOPSIS</span></span>
<span data-ttu-id="667a6-103">Sospende un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="667a6-103">Suspends an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="667a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="667a6-104">SYNTAX</span></span>

```
Suspend-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="667a6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="667a6-105">DESCRIPTION</span></span>
<span data-ttu-id="667a6-106">Il cmdlet Suspend-AzureRmAnalysisServicesServer sospende un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="667a6-106">The Suspend-AzureRmAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="667a6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="667a6-107">EXAMPLES</span></span>

### <span data-ttu-id="667a6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="667a6-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="667a6-109">Questo comando sospenderà un server attivo denominato TestServer nel ResourceGroup TestGroup</span><span class="sxs-lookup"><span data-stu-id="667a6-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="667a6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="667a6-110">PARAMETERS</span></span>

### <span data-ttu-id="667a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="667a6-111">-DefaultProfile</span></span>
<span data-ttu-id="667a6-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="667a6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="667a6-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="667a6-113">-Name</span></span>
<span data-ttu-id="667a6-114">Nome del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="667a6-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="667a6-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="667a6-115">-PassThru</span></span>
<span data-ttu-id="667a6-116">Restituirà i dettagli del server eliminati se l'operazione viene completata correttamente</span><span class="sxs-lookup"><span data-stu-id="667a6-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="667a6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="667a6-117">-ResourceGroupName</span></span>
<span data-ttu-id="667a6-118">Nome del gruppo di risorse Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="667a6-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667a6-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="667a6-119">-Confirm</span></span>
<span data-ttu-id="667a6-120">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="667a6-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="667a6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="667a6-121">-WhatIf</span></span>
<span data-ttu-id="667a6-122">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="667a6-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="667a6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="667a6-123">CommonParameters</span></span>
<span data-ttu-id="667a6-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="667a6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="667a6-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="667a6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="667a6-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="667a6-126">INPUTS</span></span>

### <span data-ttu-id="667a6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="667a6-127">System.String</span></span>

## <span data-ttu-id="667a6-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="667a6-128">OUTPUTS</span></span>

### <span data-ttu-id="667a6-129">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="667a6-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="667a6-130">Note</span><span class="sxs-lookup"><span data-stu-id="667a6-130">NOTES</span></span>
<span data-ttu-id="667a6-131">Alias: Suspend-AzureAs</span><span class="sxs-lookup"><span data-stu-id="667a6-131">Alias: Suspend-AzureAs</span></span>

## <span data-ttu-id="667a6-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="667a6-132">RELATED LINKS</span></span>

[<span data-ttu-id="667a6-133">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="667a6-133">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="667a6-134">Curriculum vitae-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="667a6-134">Resume-AzureRmAnalysisServicesServer</span></span>](./Resume-AzureRmAnalysisServicesServer.md)

