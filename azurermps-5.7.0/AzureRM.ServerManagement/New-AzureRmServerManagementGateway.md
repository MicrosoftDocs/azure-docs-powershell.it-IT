---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: D7485CB9-AE12-445B-8984-3D21FCA0E82F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
ms.openlocfilehash: f73d53fc3031fc72be950547e5b9c2b93a9a0079
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685820"
---
# <span data-ttu-id="967d2-101">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="967d2-101">New-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="967d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="967d2-102">SYNOPSIS</span></span>
<span data-ttu-id="967d2-103">Crea un gateway di gestione server.</span><span class="sxs-lookup"><span data-stu-id="967d2-103">Creates a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="967d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="967d2-104">SYNTAX</span></span>

```
New-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 [-AutoUpgrade] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="967d2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="967d2-105">DESCRIPTION</span></span>
<span data-ttu-id="967d2-106">Il cmdlet **New-AzureRmServerManagementGateway** crea un gateway di gestione di Azure server.</span><span class="sxs-lookup"><span data-stu-id="967d2-106">The **New-AzureRmServerManagementGateway** cmdlet creates an Azure Server Management gateway.</span></span>

## <span data-ttu-id="967d2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="967d2-107">EXAMPLES</span></span>

## <span data-ttu-id="967d2-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="967d2-108">PARAMETERS</span></span>

### <span data-ttu-id="967d2-109">-Autoupgrade</span><span class="sxs-lookup"><span data-stu-id="967d2-109">-AutoUpgrade</span></span>
<span data-ttu-id="967d2-110">Indica che il gateway si aggiornerà automaticamente quando viene rilasciata una nuova versione.</span><span class="sxs-lookup"><span data-stu-id="967d2-110">Indicates that the gateway will auto upgrade itself when a new version is released.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="967d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="967d2-111">-DefaultProfile</span></span>
<span data-ttu-id="967d2-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="967d2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="967d2-113">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="967d2-113">-GatewayName</span></span>
<span data-ttu-id="967d2-114">Specifica il nome del gateway creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="967d2-114">Specifies the name of the gateway that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="967d2-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="967d2-115">-Location</span></span>
<span data-ttu-id="967d2-116">Specifica la posizione in cui creare il gateway.</span><span class="sxs-lookup"><span data-stu-id="967d2-116">Specifies the location in which to create the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="967d2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="967d2-117">-ResourceGroupName</span></span>
<span data-ttu-id="967d2-118">Specifica il nome del gruppo di risorse in cui questo cmdlet crea il gateway.</span><span class="sxs-lookup"><span data-stu-id="967d2-118">Specifies the name of the resource group in which this cmdlet creates the gateway.</span></span>

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

### <span data-ttu-id="967d2-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="967d2-119">-Tag</span></span>
<span data-ttu-id="967d2-120">Coppie chiave/valore associate al gateway.</span><span class="sxs-lookup"><span data-stu-id="967d2-120">Key/value pairs associated with the gateway.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="967d2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="967d2-121">CommonParameters</span></span>
<span data-ttu-id="967d2-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="967d2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="967d2-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="967d2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="967d2-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="967d2-124">INPUTS</span></span>

### <span data-ttu-id="967d2-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="967d2-125">None</span></span>
<span data-ttu-id="967d2-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="967d2-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="967d2-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="967d2-127">OUTPUTS</span></span>

### <span data-ttu-id="967d2-128">Microsoft. Azure. Commands. ServerManagement. Model. gateway</span><span class="sxs-lookup"><span data-stu-id="967d2-128">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="967d2-129">Note</span><span class="sxs-lookup"><span data-stu-id="967d2-129">NOTES</span></span>

## <span data-ttu-id="967d2-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="967d2-130">RELATED LINKS</span></span>

[<span data-ttu-id="967d2-131">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="967d2-131">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="967d2-132">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="967d2-132">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


