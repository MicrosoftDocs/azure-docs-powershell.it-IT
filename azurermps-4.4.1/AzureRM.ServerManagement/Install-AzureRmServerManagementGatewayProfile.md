---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 06081209-BBE5-4F76-86F8-9CF6197938F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: b1d3d757d7970a21a2d81af9f1e08d0d8126df96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686152"
---
# <span data-ttu-id="692ae-101">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="692ae-101">Install-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="692ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="692ae-102">SYNOPSIS</span></span>
<span data-ttu-id="692ae-103">Installa un profilo del gateway di gestione server.</span><span class="sxs-lookup"><span data-stu-id="692ae-103">Installs a Server Management Gateway profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="692ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="692ae-104">SYNTAX</span></span>

```
Install-AzureRmServerManagementGatewayProfile [[-InputFile] <FileInfo>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="692ae-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="692ae-105">DESCRIPTION</span></span>
<span data-ttu-id="692ae-106">Il cmdlet **Install-AzureRmServerManagementGatewayProfile** installa un profilo del gateway di gestione di Azure server nella posizione corretta.</span><span class="sxs-lookup"><span data-stu-id="692ae-106">The **Install-AzureRmServerManagementGatewayProfile** cmdlet installs an Azure Server Management Gateway profile into the correct location.</span></span>
<span data-ttu-id="692ae-107">Il file installato da questo cmdlet è denominato profile.jsattivato.</span><span class="sxs-lookup"><span data-stu-id="692ae-107">The file that this cmdlet installs is named profile.json.</span></span>

## <span data-ttu-id="692ae-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="692ae-108">EXAMPLES</span></span>

## <span data-ttu-id="692ae-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="692ae-109">PARAMETERS</span></span>

### <span data-ttu-id="692ae-110">-InputFile</span><span class="sxs-lookup"><span data-stu-id="692ae-110">-InputFile</span></span>
<span data-ttu-id="692ae-111">Specifica il nome del file locale che contiene il profilo del gateway da installare.</span><span class="sxs-lookup"><span data-stu-id="692ae-111">Specifies the name of the local file that contains the gateway profile to install.</span></span>

<span data-ttu-id="692ae-112">Il file installato dal cmdlet deve essere stato salvato in precedenza con il cmdlet Save-AzureRmServerManagementGatewayProfile.</span><span class="sxs-lookup"><span data-stu-id="692ae-112">The file that this cmdlet installs should have been previously saved with the Save-AzureRmServerManagementGatewayProfile cmdlet.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="692ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="692ae-113">-DefaultProfile</span></span>
<span data-ttu-id="692ae-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="692ae-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="692ae-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="692ae-115">CommonParameters</span></span>
<span data-ttu-id="692ae-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="692ae-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="692ae-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="692ae-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="692ae-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="692ae-118">INPUTS</span></span>

### <span data-ttu-id="692ae-119">FileInfo</span><span class="sxs-lookup"><span data-stu-id="692ae-119">FileInfo</span></span>
<span data-ttu-id="692ae-120">Il parametro ' InputFile ' accetta il valore di tipo ' FileInfo ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="692ae-120">Parameter 'InputFile' accepts value of type 'FileInfo' from the pipeline</span></span>

## <span data-ttu-id="692ae-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="692ae-121">OUTPUTS</span></span>

## <span data-ttu-id="692ae-122">Note</span><span class="sxs-lookup"><span data-stu-id="692ae-122">NOTES</span></span>

## <span data-ttu-id="692ae-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="692ae-123">RELATED LINKS</span></span>

[<span data-ttu-id="692ae-124">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="692ae-124">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="692ae-125">Salva-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="692ae-125">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


