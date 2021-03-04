---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/suspend-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
ms.openlocfilehash: 9130c86662136845f1222e2c35ab93cbf32acfb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959277"
---
# <span data-ttu-id="d4069-101">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d4069-101">Suspend-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="d4069-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4069-102">SYNOPSIS</span></span>
<span data-ttu-id="d4069-103">Sospende un'istanza del server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="d4069-103">Suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="d4069-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4069-104">SYNTAX</span></span>

```
Suspend-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4069-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d4069-105">DESCRIPTION</span></span>
<span data-ttu-id="d4069-106">Il cmdlet Suspend-AzAnalysisServicesServer sospende un'istanza del server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="d4069-106">The Suspend-AzAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="d4069-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4069-107">EXAMPLES</span></span>

### <span data-ttu-id="d4069-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d4069-108">Example 1</span></span>
```
PS C:\> Suspend-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="d4069-109">Questo comando sospenderà un server attivo denominato testserver nel gruppo di test del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d4069-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="d4069-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4069-110">PARAMETERS</span></span>

### <span data-ttu-id="d4069-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4069-111">-DefaultProfile</span></span>
<span data-ttu-id="d4069-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4069-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4069-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d4069-113">-Name</span></span>
<span data-ttu-id="d4069-114">Nome del server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="d4069-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="d4069-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4069-115">-PassThru</span></span>
<span data-ttu-id="d4069-116">Restituirà i dettagli del server eliminati se l'operazione viene completata correttamente</span><span class="sxs-lookup"><span data-stu-id="d4069-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="d4069-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4069-117">-ResourceGroupName</span></span>
<span data-ttu-id="d4069-118">Nome del gruppo di risorse di Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="d4069-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="d4069-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4069-119">-Confirm</span></span>
<span data-ttu-id="d4069-120">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="d4069-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="d4069-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4069-121">-WhatIf</span></span>
<span data-ttu-id="d4069-122">Descrive le azioni che l'operazione corrente eseguirà senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="d4069-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="d4069-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4069-123">CommonParameters</span></span>
<span data-ttu-id="d4069-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4069-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4069-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4069-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4069-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="d4069-126">INPUTS</span></span>

### <span data-ttu-id="d4069-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d4069-127">System.String</span></span>

## <span data-ttu-id="d4069-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4069-128">OUTPUTS</span></span>

### <span data-ttu-id="d4069-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d4069-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="d4069-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="d4069-130">NOTES</span></span>
<span data-ttu-id="d4069-131">Alias: Suspend-AzAs</span><span class="sxs-lookup"><span data-stu-id="d4069-131">Alias: Suspend-AzAs</span></span>

## <span data-ttu-id="d4069-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4069-132">RELATED LINKS</span></span>

[<span data-ttu-id="d4069-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d4069-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="d4069-134">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d4069-134">Resume-AzAnalysisServicesServer</span></span>](./Resume-AzAnalysisServicesServer.md)

