---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 8e5041b57c4063a3d1ceb2f62e0149132c21b953
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519656"
---
# <span data-ttu-id="6cc4f-101">Test-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6cc4f-101">Test-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="6cc4f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6cc4f-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc4f-103">Verifica l'esistenza di un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="6cc4f-103">Tests the existence of an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cc4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6cc4f-104">SYNTAX</span></span>

```
Test-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cc4f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6cc4f-105">DESCRIPTION</span></span>
<span data-ttu-id="6cc4f-106">Il cmdlet Test-AzureRmAnalysisServicesServer verifica l'esistenza di un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="6cc4f-106">The Test-AzureRmAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="6cc4f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6cc4f-107">EXAMPLES</span></span>

### <span data-ttu-id="6cc4f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6cc4f-108">Example 1</span></span>
```
PS C:\> Test-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="6cc4f-109">Questo comando testerà se esiste un server denominato TestServer nel ResourceGroup TestGroup</span><span class="sxs-lookup"><span data-stu-id="6cc4f-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="6cc4f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6cc4f-110">PARAMETERS</span></span>

### <span data-ttu-id="6cc4f-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="6cc4f-111">-Name</span></span>
<span data-ttu-id="6cc4f-112">Nome del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="6cc4f-112">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="6cc4f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cc4f-113">-ResourceGroupName</span></span>
<span data-ttu-id="6cc4f-114">Nome del gruppo di risorse Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="6cc4f-114">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="6cc4f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc4f-115">-DefaultProfile</span></span>
<span data-ttu-id="6cc4f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6cc4f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cc4f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc4f-117">CommonParameters</span></span>
<span data-ttu-id="6cc4f-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cc4f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc4f-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cc4f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc4f-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6cc4f-120">INPUTS</span></span>

## <span data-ttu-id="6cc4f-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6cc4f-121">OUTPUTS</span></span>

### <span data-ttu-id="6cc4f-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6cc4f-122">System.Boolean</span></span>

## <span data-ttu-id="6cc4f-123">Note</span><span class="sxs-lookup"><span data-stu-id="6cc4f-123">NOTES</span></span>
<span data-ttu-id="6cc4f-124">Alias: Test-AzureAs</span><span class="sxs-lookup"><span data-stu-id="6cc4f-124">Alias: Test-AzureAs</span></span>

## <span data-ttu-id="6cc4f-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6cc4f-125">RELATED LINKS</span></span>

[<span data-ttu-id="6cc4f-126">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6cc4f-126">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="6cc4f-127">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6cc4f-127">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
