---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmDnsAvailability.md
ms.openlocfilehash: 348fd7e97566520b27163de91d4d52162d4c3978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517423"
---
# <span data-ttu-id="d9d6f-101">Test-AzureRmDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="d9d6f-101">Test-AzureRmDnsAvailability</span></span>

## <span data-ttu-id="d9d6f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="d9d6f-103">Controlla se un nome di dominio nella zona cloudapp.azure.com è disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="d9d6f-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9d6f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9d6f-104">SYNTAX</span></span>

```
Test-AzureRmDnsAvailability -DomainNameLabel <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9d6f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9d6f-105">DESCRIPTION</span></span>
<span data-ttu-id="d9d6f-106">Controlla se un nome di dominio nella zona cloudapp.azure.com è disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="d9d6f-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="d9d6f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9d6f-107">EXAMPLES</span></span>

### <span data-ttu-id="d9d6f-108">Esempio 1: verificare se contoso.cloudapp.azure.com è disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="d9d6f-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzureRmDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="d9d6f-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9d6f-109">PARAMETERS</span></span>

### <span data-ttu-id="d9d6f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9d6f-110">-DefaultProfile</span></span>
<span data-ttu-id="d9d6f-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9d6f-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9d6f-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="d9d6f-112">-DomainNameLabel</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainQualifiedName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9d6f-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d9d6f-113">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9d6f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9d6f-114">CommonParameters</span></span>
<span data-ttu-id="d9d6f-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9d6f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9d6f-116">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9d6f-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9d6f-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9d6f-117">INPUTS</span></span>

### <span data-ttu-id="d9d6f-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d9d6f-118">None</span></span>

## <span data-ttu-id="d9d6f-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9d6f-119">OUTPUTS</span></span>

### <span data-ttu-id="d9d6f-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d9d6f-120">System.Boolean</span></span>

## <span data-ttu-id="d9d6f-121">Note</span><span class="sxs-lookup"><span data-stu-id="d9d6f-121">NOTES</span></span>

## <span data-ttu-id="d9d6f-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9d6f-122">RELATED LINKS</span></span>
