---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: b51c41ddd36d19afedd0091be9b0a00bb447faaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964621"
---
# <span data-ttu-id="9bca0-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="9bca0-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="9bca0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bca0-102">SYNOPSIS</span></span>
<span data-ttu-id="9bca0-103">Recupera tutte le SKU valide a cui può essere transizione questo IotHub.</span><span class="sxs-lookup"><span data-stu-id="9bca0-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="9bca0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9bca0-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9bca0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9bca0-105">DESCRIPTION</span></span>
<span data-ttu-id="9bca0-106">Ottiene tutte le SKU valide a cui può essere transizione questo IotHub.</span><span class="sxs-lookup"><span data-stu-id="9bca0-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="9bca0-107">Non è possibile passare da una SKU gratuita a un'altra e viceversa.</span><span class="sxs-lookup"><span data-stu-id="9bca0-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="9bca0-108">Per ottenere questo risultato sarà necessario eliminare e ricreare il file iothub.</span><span class="sxs-lookup"><span data-stu-id="9bca0-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="9bca0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9bca0-109">EXAMPLES</span></span>

### <span data-ttu-id="9bca0-110">Esempio 1: Ottenere le SKU valide</span><span class="sxs-lookup"><span data-stu-id="9bca0-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="9bca0-111">Ottiene un elenco di tutte le SKU per i dati di IotHub denominati "myiothub"</span><span class="sxs-lookup"><span data-stu-id="9bca0-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="9bca0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bca0-112">PARAMETERS</span></span>

### <span data-ttu-id="9bca0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bca0-113">-DefaultProfile</span></span>
<span data-ttu-id="9bca0-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9bca0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9bca0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9bca0-115">-Name</span></span>
<span data-ttu-id="9bca0-116">Nome dell'hub IoT.</span><span class="sxs-lookup"><span data-stu-id="9bca0-116">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bca0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bca0-117">-ResourceGroupName</span></span>
<span data-ttu-id="9bca0-118">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9bca0-118">Resource Group Name</span></span>

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

### <span data-ttu-id="9bca0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bca0-119">CommonParameters</span></span>
<span data-ttu-id="9bca0-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bca0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bca0-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bca0-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bca0-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="9bca0-122">INPUTS</span></span>

### <span data-ttu-id="9bca0-123">System.String</span><span class="sxs-lookup"><span data-stu-id="9bca0-123">System.String</span></span>

## <span data-ttu-id="9bca0-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9bca0-124">OUTPUTS</span></span>

### <span data-ttu-id="9bca0-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="9bca0-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="9bca0-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="9bca0-126">NOTES</span></span>

## <span data-ttu-id="9bca0-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9bca0-127">RELATED LINKS</span></span>
