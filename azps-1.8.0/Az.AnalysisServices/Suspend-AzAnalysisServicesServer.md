---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/suspend-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
ms.openlocfilehash: ecd9e83607da048246ec996188fd9a31d231ff32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673679"
---
# <span data-ttu-id="c2623-101">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c2623-101">Suspend-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="c2623-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2623-102">SYNOPSIS</span></span>
<span data-ttu-id="c2623-103">Sospende un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="c2623-103">Suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="c2623-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2623-104">SYNTAX</span></span>

```
Suspend-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2623-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2623-105">DESCRIPTION</span></span>
<span data-ttu-id="c2623-106">Il cmdlet Suspend-AzAnalysisServicesServer sospende un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="c2623-106">The Suspend-AzAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="c2623-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2623-107">EXAMPLES</span></span>

### <span data-ttu-id="c2623-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c2623-108">Example 1</span></span>
```
PS C:\> Suspend-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="c2623-109">Questo comando sospenderà un server attivo denominato TestServer nel ResourceGroup TestGroup</span><span class="sxs-lookup"><span data-stu-id="c2623-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="c2623-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2623-110">PARAMETERS</span></span>

### <span data-ttu-id="c2623-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2623-111">-DefaultProfile</span></span>
<span data-ttu-id="c2623-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2623-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2623-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2623-113">-Name</span></span>
<span data-ttu-id="c2623-114">Nome del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="c2623-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="c2623-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2623-115">-PassThru</span></span>
<span data-ttu-id="c2623-116">Restituirà i dettagli del server eliminati se l'operazione viene completata correttamente</span><span class="sxs-lookup"><span data-stu-id="c2623-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="c2623-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2623-117">-ResourceGroupName</span></span>
<span data-ttu-id="c2623-118">Nome del gruppo di risorse Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="c2623-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="c2623-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c2623-119">-Confirm</span></span>
<span data-ttu-id="c2623-120">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="c2623-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="c2623-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2623-121">-WhatIf</span></span>
<span data-ttu-id="c2623-122">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="c2623-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="c2623-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2623-123">CommonParameters</span></span>
<span data-ttu-id="c2623-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2623-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2623-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2623-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2623-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2623-126">INPUTS</span></span>

### <span data-ttu-id="c2623-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c2623-127">System.String</span></span>

## <span data-ttu-id="c2623-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2623-128">OUTPUTS</span></span>

### <span data-ttu-id="c2623-129">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c2623-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="c2623-130">Note</span><span class="sxs-lookup"><span data-stu-id="c2623-130">NOTES</span></span>
<span data-ttu-id="c2623-131">Alias: Suspend-AzAs</span><span class="sxs-lookup"><span data-stu-id="c2623-131">Alias: Suspend-AzAs</span></span>

## <span data-ttu-id="c2623-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2623-132">RELATED LINKS</span></span>

[<span data-ttu-id="c2623-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c2623-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="c2623-134">Curriculum vitae-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c2623-134">Resume-AzAnalysisServicesServer</span></span>](./Resume-AzAnalysisServicesServer.md)

