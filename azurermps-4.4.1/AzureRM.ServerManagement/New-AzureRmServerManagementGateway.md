---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: D7485CB9-AE12-445B-8984-3D21FCA0E82F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
ms.openlocfilehash: 9cb98b9671f43ddd7acbcc84e8473a12da00f405
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516027"
---
# <span data-ttu-id="2a12f-101">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="2a12f-101">New-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="2a12f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2a12f-102">SYNOPSIS</span></span>
<span data-ttu-id="2a12f-103">Crea un gateway di gestione server.</span><span class="sxs-lookup"><span data-stu-id="2a12f-103">Creates a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a12f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a12f-104">SYNTAX</span></span>

```
New-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 [-AutoUpgrade] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a12f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a12f-105">DESCRIPTION</span></span>
<span data-ttu-id="2a12f-106">Il cmdlet **New-AzureRmServerManagementGateway** crea un gateway di gestione di Azure server.</span><span class="sxs-lookup"><span data-stu-id="2a12f-106">The **New-AzureRmServerManagementGateway** cmdlet creates an Azure Server Management gateway.</span></span>

## <span data-ttu-id="2a12f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a12f-107">EXAMPLES</span></span>

## <span data-ttu-id="2a12f-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a12f-108">PARAMETERS</span></span>

### <span data-ttu-id="2a12f-109">-Autoupgrade</span><span class="sxs-lookup"><span data-stu-id="2a12f-109">-AutoUpgrade</span></span>
<span data-ttu-id="2a12f-110">Indica che il gateway si aggiornerà automaticamente quando viene rilasciata una nuova versione.</span><span class="sxs-lookup"><span data-stu-id="2a12f-110">Indicates that the gateway will auto upgrade itself when a new version is released.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a12f-111">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="2a12f-111">-GatewayName</span></span>
<span data-ttu-id="2a12f-112">Specifica il nome del gateway creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a12f-112">Specifies the name of the gateway that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2a12f-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2a12f-113">-Location</span></span>
<span data-ttu-id="2a12f-114">Specifica la posizione in cui creare il gateway.</span><span class="sxs-lookup"><span data-stu-id="2a12f-114">Specifies the location in which to create the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a12f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a12f-115">-ResourceGroupName</span></span>
<span data-ttu-id="2a12f-116">Specifica il nome del gruppo di risorse in cui questo cmdlet crea il gateway.</span><span class="sxs-lookup"><span data-stu-id="2a12f-116">Specifies the name of the resource group in which this cmdlet creates the gateway.</span></span>

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

### <span data-ttu-id="2a12f-117">-Tag</span><span class="sxs-lookup"><span data-stu-id="2a12f-117">-Tags</span></span>
<span data-ttu-id="2a12f-118">Specifica i tag come coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="2a12f-118">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="2a12f-119">Puoi usare i tag per identificare un gateway da altre risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="2a12f-119">You can use tags to identify a Gateway from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a12f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a12f-120">-DefaultProfile</span></span>
<span data-ttu-id="2a12f-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a12f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a12f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a12f-122">CommonParameters</span></span>
<span data-ttu-id="2a12f-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a12f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a12f-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a12f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a12f-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2a12f-125">INPUTS</span></span>

## <span data-ttu-id="2a12f-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a12f-126">OUTPUTS</span></span>

### <span data-ttu-id="2a12f-127">Microsoft. Azure. Commands. ServerManagement. Model. gateway</span><span class="sxs-lookup"><span data-stu-id="2a12f-127">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="2a12f-128">Note</span><span class="sxs-lookup"><span data-stu-id="2a12f-128">NOTES</span></span>

## <span data-ttu-id="2a12f-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a12f-129">RELATED LINKS</span></span>

[<span data-ttu-id="2a12f-130">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="2a12f-130">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="2a12f-131">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="2a12f-131">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


