---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/remove-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
ms.openlocfilehash: 9076df0ae023539560b690723dd9abc92d922e45
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199943"
---
# <span data-ttu-id="30b8e-101">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="30b8e-101">Remove-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="30b8e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30b8e-102">SYNOPSIS</span></span>
<span data-ttu-id="30b8e-103">Elimina un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="30b8e-103">Deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="30b8e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30b8e-104">SYNTAX</span></span>

```
Remove-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30b8e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30b8e-105">DESCRIPTION</span></span>
<span data-ttu-id="30b8e-106">Il cmdlet Remove-AzAnalysisServicesServer Elimina un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="30b8e-106">The Remove-AzAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="30b8e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30b8e-107">EXAMPLES</span></span>

### <span data-ttu-id="30b8e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="30b8e-108">Example 1</span></span>
```
PS C:\> Remove-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="30b8e-109">Questo comando rimuoverà il server denominato TestServer nel ResourceGroup TestGroup</span><span class="sxs-lookup"><span data-stu-id="30b8e-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="30b8e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30b8e-110">PARAMETERS</span></span>

### <span data-ttu-id="30b8e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30b8e-111">-DefaultProfile</span></span>
<span data-ttu-id="30b8e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30b8e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30b8e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="30b8e-113">-Name</span></span>
<span data-ttu-id="30b8e-114">Nome del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="30b8e-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="30b8e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30b8e-115">-PassThru</span></span>
<span data-ttu-id="30b8e-116">Restituirà i dettagli del server eliminati se l'operazione viene completata correttamente</span><span class="sxs-lookup"><span data-stu-id="30b8e-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="30b8e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30b8e-117">-ResourceGroupName</span></span>
<span data-ttu-id="30b8e-118">Nome del gruppo di risorse Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="30b8e-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="30b8e-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="30b8e-119">-Confirm</span></span>
<span data-ttu-id="30b8e-120">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="30b8e-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="30b8e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30b8e-121">-WhatIf</span></span>
<span data-ttu-id="30b8e-122">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="30b8e-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="30b8e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30b8e-123">CommonParameters</span></span>
<span data-ttu-id="30b8e-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30b8e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30b8e-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30b8e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30b8e-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30b8e-126">INPUTS</span></span>

### <span data-ttu-id="30b8e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="30b8e-127">System.String</span></span>

## <span data-ttu-id="30b8e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30b8e-128">OUTPUTS</span></span>

### <span data-ttu-id="30b8e-129">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="30b8e-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="30b8e-130">Note</span><span class="sxs-lookup"><span data-stu-id="30b8e-130">NOTES</span></span>
<span data-ttu-id="30b8e-131">Alias: Remove-AzAs</span><span class="sxs-lookup"><span data-stu-id="30b8e-131">Alias: Remove-AzAs</span></span>

## <span data-ttu-id="30b8e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30b8e-132">RELATED LINKS</span></span>

[<span data-ttu-id="30b8e-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="30b8e-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="30b8e-134">New-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="30b8e-134">New-AzAnalysisServicesServer</span></span>](./New-AzAnalysisServicesServer.md)