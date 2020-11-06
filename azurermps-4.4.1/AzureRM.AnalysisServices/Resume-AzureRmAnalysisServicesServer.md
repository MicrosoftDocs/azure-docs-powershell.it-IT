---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 99f8eaae633f984cdd522576a3f65bf894143bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508864"
---
# <span data-ttu-id="7aff4-101">Resume-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7aff4-101">Resume-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="7aff4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7aff4-102">SYNOPSIS</span></span>
<span data-ttu-id="7aff4-103">Riprende un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="7aff4-103">Resumes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7aff4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7aff4-104">SYNTAX</span></span>

```
Resume-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7aff4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7aff4-105">DESCRIPTION</span></span>
<span data-ttu-id="7aff4-106">Il cmdlet Resume-AzureRmAnalysisServicesServer riprende un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="7aff4-106">The Resume-AzureRmAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="7aff4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7aff4-107">EXAMPLES</span></span>

### <span data-ttu-id="7aff4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7aff4-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="7aff4-109">Questo comando riprenderà un server in pausa denominato TestServer nel ResourceGroup TestGroup</span><span class="sxs-lookup"><span data-stu-id="7aff4-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="7aff4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7aff4-110">PARAMETERS</span></span>

### <span data-ttu-id="7aff4-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="7aff4-111">-Name</span></span>
<span data-ttu-id="7aff4-112">Nome del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="7aff4-112">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="7aff4-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7aff4-113">-PassThru</span></span>
<span data-ttu-id="7aff4-114">Restituirà i dettagli del server eliminati se l'operazione viene completata correttamente</span><span class="sxs-lookup"><span data-stu-id="7aff4-114">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="7aff4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7aff4-115">-ResourceGroupName</span></span>
<span data-ttu-id="7aff4-116">Nome del gruppo di risorse Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="7aff4-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="7aff4-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7aff4-117">-Confirm</span></span>
<span data-ttu-id="7aff4-118">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="7aff4-118">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="7aff4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7aff4-119">-WhatIf</span></span>
<span data-ttu-id="7aff4-120">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="7aff4-120">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="7aff4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aff4-121">CommonParameters</span></span>
<span data-ttu-id="7aff4-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7aff4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aff4-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7aff4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aff4-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7aff4-124">INPUTS</span></span>

## <span data-ttu-id="7aff4-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7aff4-125">OUTPUTS</span></span>

### <span data-ttu-id="7aff4-126">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7aff4-126">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="7aff4-127">Note</span><span class="sxs-lookup"><span data-stu-id="7aff4-127">NOTES</span></span>
<span data-ttu-id="7aff4-128">Alias: Resume-AzureAs</span><span class="sxs-lookup"><span data-stu-id="7aff4-128">Alias: Resume-AzureAs</span></span>

## <span data-ttu-id="7aff4-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7aff4-129">RELATED LINKS</span></span>

[<span data-ttu-id="7aff4-130">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7aff4-130">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="7aff4-131">Suspend-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7aff4-131">Suspend-AzureRmAnalysisServicesServer</span></span>](./Suspend-AzureRmAnalysisServicesServer.md)
