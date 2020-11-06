---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 41F8F851-6F9F-4DA4-8CE6-D8C9B7CF68D7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
ms.openlocfilehash: 2bcfac139d38f0b6f7d621a7761ce01d1d3f2f45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516023"
---
# <span data-ttu-id="39777-101">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="39777-101">Remove-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="39777-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39777-102">SYNOPSIS</span></span>
<span data-ttu-id="39777-103">Rimuove un gateway di gestione server.</span><span class="sxs-lookup"><span data-stu-id="39777-103">Removes a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39777-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39777-104">SYNTAX</span></span>

### <span data-ttu-id="39777-105">ByName</span><span class="sxs-lookup"><span data-stu-id="39777-105">ByName</span></span>
```
Remove-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39777-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="39777-106">ByObject</span></span>
```
Remove-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39777-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39777-107">DESCRIPTION</span></span>
<span data-ttu-id="39777-108">Il cmdlet **Remove-AzureRmServerManagementGateway** rimuove un gateway di gestione di Azure server.</span><span class="sxs-lookup"><span data-stu-id="39777-108">The **Remove-AzureRmServerManagementGateway** cmdlet removes an Azure Server Management gateway.</span></span>

## <span data-ttu-id="39777-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39777-109">EXAMPLES</span></span>

## <span data-ttu-id="39777-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39777-110">PARAMETERS</span></span>

### <span data-ttu-id="39777-111">-Gateway</span><span class="sxs-lookup"><span data-stu-id="39777-111">-Gateway</span></span>
<span data-ttu-id="39777-112">Specifica il gateway rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39777-112">Specifies the gateway that this cmdlet removes.</span></span>

<span data-ttu-id="39777-113">Questo parametro può essere usato al posto dei parametri *ResourceGroupName* e *GatewayName* .</span><span class="sxs-lookup"><span data-stu-id="39777-113">This parameter may be used instead of the *ResourceGroupName* and the *GatewayName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39777-114">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="39777-114">-GatewayName</span></span>
<span data-ttu-id="39777-115">Specifica il nome del gateway rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39777-115">Specifies the name of the gateway that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39777-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39777-116">-ResourceGroupName</span></span>
<span data-ttu-id="39777-117">Specifica il nome del gruppo di risorse a cui appartiene il gateway.</span><span class="sxs-lookup"><span data-stu-id="39777-117">Specifies the name of the resource group in that the gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39777-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39777-118">-DefaultProfile</span></span>
<span data-ttu-id="39777-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39777-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39777-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39777-120">CommonParameters</span></span>
<span data-ttu-id="39777-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39777-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39777-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39777-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39777-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39777-123">INPUTS</span></span>

### <span data-ttu-id="39777-124">Gateway</span><span class="sxs-lookup"><span data-stu-id="39777-124">Gateway</span></span>
<span data-ttu-id="39777-125">Il parametro "gateway" accetta il valore di tipo "gateway" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="39777-125">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="39777-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39777-126">OUTPUTS</span></span>

## <span data-ttu-id="39777-127">Note</span><span class="sxs-lookup"><span data-stu-id="39777-127">NOTES</span></span>
* <span data-ttu-id="39777-128">Tutti i nodi del gateway devono essere rimossi prima di usare questo cmdlet; in caso contrario, il cmdlet avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="39777-128">All the nodes in the Gateway must be removed before using this cmdlet; otherwise this cmdlet will fail.</span></span>

## <span data-ttu-id="39777-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39777-129">RELATED LINKS</span></span>

[<span data-ttu-id="39777-130">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="39777-130">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="39777-131">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="39777-131">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)


