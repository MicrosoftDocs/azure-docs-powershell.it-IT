---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 22B63259-799B-4F25-A06B-7A818D295870
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/reset-azurermservermanagementgatewayprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: 0833266bcd6e98a1d9744db2bc202bce5a01f3f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512304"
---
# <span data-ttu-id="df755-101">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="df755-101">Reset-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="df755-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="df755-102">SYNOPSIS</span></span>
<span data-ttu-id="df755-103">Reimposta il profilo di un gateway di gestione del server.</span><span class="sxs-lookup"><span data-stu-id="df755-103">Resets the profile of a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df755-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df755-104">SYNTAX</span></span>

### <span data-ttu-id="df755-105">ByName</span><span class="sxs-lookup"><span data-stu-id="df755-105">ByName</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df755-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="df755-106">ByObject</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df755-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df755-107">DESCRIPTION</span></span>
<span data-ttu-id="df755-108">Il cmdlet **Reset-AzureRmServerManagementGatewayProfile** Reimposta il profilo per un gateway di gestione di Azure server.</span><span class="sxs-lookup"><span data-stu-id="df755-108">The **Reset-AzureRmServerManagementGatewayProfile** cmdlet resets the profile for an Azure Server Management Gateway.</span></span>

<span data-ttu-id="df755-109">Sarà necessario usare il cmdlet Save-AzureRmServerManagementGatewayProfile per scaricare il profilo e quindi il cmdlet Install-AzureRmServerManagementGatewayProfile per salvarlo dopo la reimpostazione del profilo.</span><span class="sxs-lookup"><span data-stu-id="df755-109">You will need to use the Save-AzureRmServerManagementGatewayProfile cmdlet to download the profile and then the Install-AzureRmServerManagementGatewayProfile cmdlet to save it after you reset the profile.</span></span>

## <span data-ttu-id="df755-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df755-110">EXAMPLES</span></span>

## <span data-ttu-id="df755-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="df755-111">PARAMETERS</span></span>

### <span data-ttu-id="df755-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df755-112">-DefaultProfile</span></span>
<span data-ttu-id="df755-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="df755-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df755-114">-Gateway</span><span class="sxs-lookup"><span data-stu-id="df755-114">-Gateway</span></span>
<span data-ttu-id="df755-115">Specifica il gateway per cui il cmdlet Reimposta il profilo.</span><span class="sxs-lookup"><span data-stu-id="df755-115">Specifies the gateway for which the cmdlet resets the profile for.</span></span>

<span data-ttu-id="df755-116">Può essere specificato al posto di ResourceGoupName e GatewayName</span><span class="sxs-lookup"><span data-stu-id="df755-116">May be specified instead of ResourceGoupName and GatewayName</span></span>

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df755-117">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="df755-117">-GatewayName</span></span>
<span data-ttu-id="df755-118">Specifica il nome del gateway per cui il cmdlet Reimposta il profilo.</span><span class="sxs-lookup"><span data-stu-id="df755-118">Specifies the name of the gateway for which the cmdlet resets the profile.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df755-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df755-119">-ResourceGroupName</span></span>
<span data-ttu-id="df755-120">Specifica il nome del gruppo di risorse a cui appartiene il gateway.</span><span class="sxs-lookup"><span data-stu-id="df755-120">Specifies the name of the resource group that the gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df755-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df755-121">CommonParameters</span></span>
<span data-ttu-id="df755-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df755-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df755-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df755-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df755-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="df755-124">INPUTS</span></span>

### <span data-ttu-id="df755-125">Gateway</span><span class="sxs-lookup"><span data-stu-id="df755-125">Gateway</span></span>
<span data-ttu-id="df755-126">Il parametro "gateway" accetta il valore di tipo "gateway" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="df755-126">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="df755-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df755-127">OUTPUTS</span></span>

## <span data-ttu-id="df755-128">Note</span><span class="sxs-lookup"><span data-stu-id="df755-128">NOTES</span></span>

## <span data-ttu-id="df755-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df755-129">RELATED LINKS</span></span>

[<span data-ttu-id="df755-130">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="df755-130">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="df755-131">Salva-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="df755-131">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


