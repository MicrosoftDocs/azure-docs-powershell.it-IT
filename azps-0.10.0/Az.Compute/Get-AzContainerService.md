---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 1a0daa4bf336ba970c12c24db3d5aab73641aaea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863818"
---
# <span data-ttu-id="3b192-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="3b192-101">Get-AzContainerService</span></span>

## <span data-ttu-id="3b192-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b192-102">SYNOPSIS</span></span>
<span data-ttu-id="3b192-103">Ottiene un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="3b192-103">Gets a container service.</span></span>

## <span data-ttu-id="3b192-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b192-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b192-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b192-105">DESCRIPTION</span></span>
<span data-ttu-id="3b192-106">Il cmdlet **Get-AzContainerService** ottiene un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="3b192-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="3b192-107">È possibile visualizzare le proprietà di un servizio contenitore, che include lo stato, il numero di master e gli agenti e il nome di dominio completo di master e Agent.</span><span class="sxs-lookup"><span data-stu-id="3b192-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="3b192-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b192-108">EXAMPLES</span></span>

### <span data-ttu-id="3b192-109">Esempio 1: ottenere un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="3b192-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="3b192-110">Questo comando ottiene un servizio contenitore denominato CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="3b192-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="3b192-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b192-111">PARAMETERS</span></span>

### <span data-ttu-id="3b192-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b192-112">-DefaultProfile</span></span>
<span data-ttu-id="3b192-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b192-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b192-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="3b192-114">-Name</span></span>
<span data-ttu-id="3b192-115">Specifica il nome del servizio contenitore ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b192-115">Specifies the name of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3b192-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b192-116">-ResourceGroupName</span></span>
<span data-ttu-id="3b192-117">Specifica il gruppo di risorse del servizio contenitore ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b192-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3b192-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b192-118">CommonParameters</span></span>
<span data-ttu-id="3b192-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b192-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b192-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b192-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b192-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b192-121">INPUTS</span></span>

### <span data-ttu-id="3b192-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3b192-122">None</span></span>
<span data-ttu-id="3b192-123">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3b192-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3b192-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b192-124">OUTPUTS</span></span>

### <span data-ttu-id="3b192-125">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="3b192-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="3b192-126">Note</span><span class="sxs-lookup"><span data-stu-id="3b192-126">NOTES</span></span>

## <span data-ttu-id="3b192-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b192-127">RELATED LINKS</span></span>

[<span data-ttu-id="3b192-128">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="3b192-128">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="3b192-129">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="3b192-129">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="3b192-130">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="3b192-130">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


