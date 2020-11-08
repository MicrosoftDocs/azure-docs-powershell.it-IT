---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/resume-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
ms.openlocfilehash: 3614c62af825b109b224d231d89dda315a7e2616
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190634"
---
# <span data-ttu-id="0680c-101">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0680c-101">Resume-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="0680c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0680c-102">SYNOPSIS</span></span>
<span data-ttu-id="0680c-103">Riprende un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="0680c-103">Resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="0680c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0680c-104">SYNTAX</span></span>

```
Resume-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0680c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0680c-105">DESCRIPTION</span></span>
<span data-ttu-id="0680c-106">Il cmdlet Resume-AzAnalysisServicesServer riprende un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="0680c-106">The Resume-AzAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="0680c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0680c-107">EXAMPLES</span></span>

### <span data-ttu-id="0680c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0680c-108">Example 1</span></span>
```
PS C:\> Resume-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="0680c-109">Questo comando riprenderà un server in pausa denominato TestServer nel ResourceGroup TestGroup</span><span class="sxs-lookup"><span data-stu-id="0680c-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="0680c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0680c-110">PARAMETERS</span></span>

### <span data-ttu-id="0680c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0680c-111">-DefaultProfile</span></span>
<span data-ttu-id="0680c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0680c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0680c-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="0680c-113">-Name</span></span>
<span data-ttu-id="0680c-114">Nome del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="0680c-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="0680c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0680c-115">-PassThru</span></span>
<span data-ttu-id="0680c-116">Restituirà i dettagli del server eliminati se l'operazione viene completata correttamente</span><span class="sxs-lookup"><span data-stu-id="0680c-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="0680c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0680c-117">-ResourceGroupName</span></span>
<span data-ttu-id="0680c-118">Nome del gruppo di risorse Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="0680c-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="0680c-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0680c-119">-Confirm</span></span>
<span data-ttu-id="0680c-120">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="0680c-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="0680c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0680c-121">-WhatIf</span></span>
<span data-ttu-id="0680c-122">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="0680c-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="0680c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0680c-123">CommonParameters</span></span>
<span data-ttu-id="0680c-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0680c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0680c-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0680c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0680c-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0680c-126">INPUTS</span></span>

### <span data-ttu-id="0680c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0680c-127">System.String</span></span>

## <span data-ttu-id="0680c-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0680c-128">OUTPUTS</span></span>

### <span data-ttu-id="0680c-129">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0680c-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="0680c-130">Note</span><span class="sxs-lookup"><span data-stu-id="0680c-130">NOTES</span></span>
<span data-ttu-id="0680c-131">Alias: Resume-AzAs</span><span class="sxs-lookup"><span data-stu-id="0680c-131">Alias: Resume-AzAs</span></span>

## <span data-ttu-id="0680c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0680c-132">RELATED LINKS</span></span>

[<span data-ttu-id="0680c-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0680c-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="0680c-134">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0680c-134">Suspend-AzAnalysisServicesServer</span></span>](./Suspend-AzAnalysisServicesServer.md)
