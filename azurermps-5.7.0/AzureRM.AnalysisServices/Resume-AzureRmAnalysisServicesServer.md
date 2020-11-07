---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/resume-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 5d3d2c4d630ccb31d3d59a610881aa92a4e8b844
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686751"
---
# <span data-ttu-id="7b235-101">Resume-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7b235-101">Resume-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="7b235-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b235-102">SYNOPSIS</span></span>
<span data-ttu-id="7b235-103">Riprende un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="7b235-103">Resumes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b235-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b235-104">SYNTAX</span></span>

```
Resume-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b235-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b235-105">DESCRIPTION</span></span>
<span data-ttu-id="7b235-106">Il cmdlet Resume-AzureRmAnalysisServicesServer riprende un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="7b235-106">The Resume-AzureRmAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="7b235-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b235-107">EXAMPLES</span></span>

### <span data-ttu-id="7b235-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7b235-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="7b235-109">Questo comando riprenderà un server in pausa denominato TestServer nel ResourceGroup TestGroup</span><span class="sxs-lookup"><span data-stu-id="7b235-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="7b235-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b235-110">PARAMETERS</span></span>

### <span data-ttu-id="7b235-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b235-111">-DefaultProfile</span></span>
<span data-ttu-id="7b235-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b235-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b235-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b235-113">-Name</span></span>
<span data-ttu-id="7b235-114">Nome del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="7b235-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="7b235-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b235-115">-PassThru</span></span>
<span data-ttu-id="7b235-116">Restituirà i dettagli del server eliminati se l'operazione viene completata correttamente</span><span class="sxs-lookup"><span data-stu-id="7b235-116">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b235-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b235-117">-ResourceGroupName</span></span>
<span data-ttu-id="7b235-118">Nome del gruppo di risorse Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="7b235-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b235-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7b235-119">-Confirm</span></span>
<span data-ttu-id="7b235-120">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="7b235-120">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b235-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b235-121">-WhatIf</span></span>
<span data-ttu-id="7b235-122">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="7b235-122">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b235-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b235-123">CommonParameters</span></span>
<span data-ttu-id="7b235-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b235-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b235-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b235-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b235-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b235-126">INPUTS</span></span>

### <span data-ttu-id="7b235-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7b235-127">None</span></span>
<span data-ttu-id="7b235-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7b235-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7b235-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b235-129">OUTPUTS</span></span>

### <span data-ttu-id="7b235-130">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7b235-130">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="7b235-131">Note</span><span class="sxs-lookup"><span data-stu-id="7b235-131">NOTES</span></span>
<span data-ttu-id="7b235-132">Alias: Resume-AzureAs</span><span class="sxs-lookup"><span data-stu-id="7b235-132">Alias: Resume-AzureAs</span></span>

## <span data-ttu-id="7b235-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b235-133">RELATED LINKS</span></span>

[<span data-ttu-id="7b235-134">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7b235-134">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="7b235-135">Suspend-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7b235-135">Suspend-AzureRmAnalysisServicesServer</span></span>](./Suspend-AzureRmAnalysisServicesServer.md)
