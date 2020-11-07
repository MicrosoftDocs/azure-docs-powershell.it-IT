---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/remove-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 4976c34437b2f858f8e76924754fe04a8b1e0a84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517719"
---
# <span data-ttu-id="5f33f-101">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="5f33f-101">Remove-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="5f33f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5f33f-102">SYNOPSIS</span></span>
<span data-ttu-id="5f33f-103">Elimina un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="5f33f-103">Deletes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f33f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f33f-104">SYNTAX</span></span>

```
Remove-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f33f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f33f-105">DESCRIPTION</span></span>
<span data-ttu-id="5f33f-106">Il cmdlet Remove-AzureRmAnalysisServicesServer Elimina un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="5f33f-106">The Remove-AzureRmAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="5f33f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f33f-107">EXAMPLES</span></span>

### <span data-ttu-id="5f33f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5f33f-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="5f33f-109">Questo comando rimuoverà il server denominato TestServer nel ResourceGroup TestGroup</span><span class="sxs-lookup"><span data-stu-id="5f33f-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="5f33f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f33f-110">PARAMETERS</span></span>

### <span data-ttu-id="5f33f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f33f-111">-DefaultProfile</span></span>
<span data-ttu-id="5f33f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5f33f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f33f-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f33f-113">-Name</span></span>
<span data-ttu-id="5f33f-114">Nome del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="5f33f-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="5f33f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5f33f-115">-PassThru</span></span>
<span data-ttu-id="5f33f-116">Restituirà i dettagli del server eliminati se l'operazione viene completata correttamente</span><span class="sxs-lookup"><span data-stu-id="5f33f-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="5f33f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f33f-117">-ResourceGroupName</span></span>
<span data-ttu-id="5f33f-118">Nome del gruppo di risorse Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="5f33f-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="5f33f-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5f33f-119">-Confirm</span></span>
<span data-ttu-id="5f33f-120">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="5f33f-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="5f33f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f33f-121">-WhatIf</span></span>
<span data-ttu-id="5f33f-122">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="5f33f-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="5f33f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f33f-123">CommonParameters</span></span>
<span data-ttu-id="5f33f-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f33f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f33f-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f33f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f33f-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5f33f-126">INPUTS</span></span>

### <span data-ttu-id="5f33f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5f33f-127">System.String</span></span>

## <span data-ttu-id="5f33f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f33f-128">OUTPUTS</span></span>

### <span data-ttu-id="5f33f-129">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="5f33f-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="5f33f-130">Note</span><span class="sxs-lookup"><span data-stu-id="5f33f-130">NOTES</span></span>
<span data-ttu-id="5f33f-131">Alias: Remove-AzureAs</span><span class="sxs-lookup"><span data-stu-id="5f33f-131">Alias: Remove-AzureAs</span></span>

## <span data-ttu-id="5f33f-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f33f-132">RELATED LINKS</span></span>

[<span data-ttu-id="5f33f-133">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="5f33f-133">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="5f33f-134">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="5f33f-134">New-AzureRmAnalysisServicesServer</span></span>](./New-AzureRmAnalysisServicesServer.md)