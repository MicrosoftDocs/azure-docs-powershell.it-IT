---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 5db21871b84801d57deebf98e27bbe153285631a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867155"
---
# <span data-ttu-id="e3106-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e3106-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="e3106-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3106-102">SYNOPSIS</span></span>
<span data-ttu-id="e3106-103">Ottiene un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="e3106-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3106-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3106-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3106-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3106-105">DESCRIPTION</span></span>
<span data-ttu-id="e3106-106">Il cmdlet **Get-AzureRmContainerService** ottiene un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="e3106-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="e3106-107">È possibile visualizzare le proprietà di un servizio contenitore, che include lo stato, il numero di master e gli agenti e il nome di dominio completo di master e Agent.</span><span class="sxs-lookup"><span data-stu-id="e3106-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="e3106-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3106-108">EXAMPLES</span></span>

### <span data-ttu-id="e3106-109">Esempio 1: ottenere un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="e3106-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="e3106-110">Questo comando ottiene un servizio contenitore denominato CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="e3106-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="e3106-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3106-111">PARAMETERS</span></span>

### <span data-ttu-id="e3106-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3106-112">-DefaultProfile</span></span>
<span data-ttu-id="e3106-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3106-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3106-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3106-114">-Name</span></span>
<span data-ttu-id="e3106-115">Specifica il nome del servizio contenitore ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3106-115">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3106-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3106-116">-ResourceGroupName</span></span>
<span data-ttu-id="e3106-117">Specifica il gruppo di risorse del servizio contenitore ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3106-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e3106-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3106-118">CommonParameters</span></span>
<span data-ttu-id="e3106-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3106-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3106-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3106-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3106-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3106-121">INPUTS</span></span>

### <span data-ttu-id="e3106-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e3106-122">None</span></span>
<span data-ttu-id="e3106-123">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e3106-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e3106-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3106-124">OUTPUTS</span></span>

### <span data-ttu-id="e3106-125">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="e3106-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="e3106-126">Note</span><span class="sxs-lookup"><span data-stu-id="e3106-126">NOTES</span></span>

## <span data-ttu-id="e3106-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3106-127">RELATED LINKS</span></span>

[<span data-ttu-id="e3106-128">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e3106-128">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="e3106-129">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e3106-129">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="e3106-130">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e3106-130">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


