---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: 2ee468c47f22e90ce47b003dcae1becfb905134e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363383"
---
# <span data-ttu-id="96616-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="96616-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="96616-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96616-102">SYNOPSIS</span></span>
<span data-ttu-id="96616-103">Controlla se un nome di dominio nella zona cloudapp.azure.com è disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="96616-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="96616-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96616-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96616-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96616-105">DESCRIPTION</span></span>
<span data-ttu-id="96616-106">Controlla se un nome di dominio nella zona cloudapp.azure.com è disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="96616-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="96616-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96616-107">EXAMPLES</span></span>

### <span data-ttu-id="96616-108">Esempio 1: verificare se contoso.westus.cloudapp.azure.com è disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="96616-108">Example 1: Check if contoso.westus.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="96616-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96616-109">PARAMETERS</span></span>

### <span data-ttu-id="96616-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96616-110">-DefaultProfile</span></span>
<span data-ttu-id="96616-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96616-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96616-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="96616-112">-DomainNameLabel</span></span>
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

### <span data-ttu-id="96616-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="96616-113">-Location</span></span>
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

### <span data-ttu-id="96616-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96616-114">CommonParameters</span></span>
<span data-ttu-id="96616-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96616-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96616-116">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96616-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96616-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96616-117">INPUTS</span></span>

### <span data-ttu-id="96616-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="96616-118">None</span></span>

## <span data-ttu-id="96616-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96616-119">OUTPUTS</span></span>

### <span data-ttu-id="96616-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="96616-120">System.Boolean</span></span>

## <span data-ttu-id="96616-121">Note</span><span class="sxs-lookup"><span data-stu-id="96616-121">NOTES</span></span>

## <span data-ttu-id="96616-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96616-122">RELATED LINKS</span></span>
