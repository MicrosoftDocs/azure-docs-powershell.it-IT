---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: f443928a8a616e8b8c6c13e5ae941aff607638ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323254"
---
# <span data-ttu-id="db600-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="db600-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="db600-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db600-102">SYNOPSIS</span></span>
<span data-ttu-id="db600-103">**Test-AzPrivateLinkServiceVisibility** controlla se un servizio di collegamento privato è visibile per l'uso corrente.</span><span class="sxs-lookup"><span data-stu-id="db600-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="db600-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db600-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db600-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db600-105">DESCRIPTION</span></span>
<span data-ttu-id="db600-106">Verificare se un servizio di collegamento privato è visibile per l'uso corrente.</span><span class="sxs-lookup"><span data-stu-id="db600-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="db600-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db600-107">EXAMPLES</span></span>

### <span data-ttu-id="db600-108">Esempio 1: verificare se contoso.cloudapp.azure.com è disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="db600-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="db600-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db600-109">PARAMETERS</span></span>

### <span data-ttu-id="db600-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db600-110">-DefaultProfile</span></span>
<span data-ttu-id="db600-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db600-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db600-112">-Posizione</span><span class="sxs-lookup"><span data-stu-id="db600-112">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db600-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="db600-113">-PrivateLinkServiceAlias</span></span>
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

### <span data-ttu-id="db600-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db600-114">-ResourceGroupName</span></span>
<span data-ttu-id="db600-115">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="db600-115">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db600-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db600-116">CommonParameters</span></span>
<span data-ttu-id="db600-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db600-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db600-118">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db600-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db600-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db600-119">INPUTS</span></span>

### <span data-ttu-id="db600-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="db600-120">None</span></span>

## <span data-ttu-id="db600-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db600-121">OUTPUTS</span></span>

### <span data-ttu-id="db600-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="db600-122">System.Boolean</span></span>

## <span data-ttu-id="db600-123">Note</span><span class="sxs-lookup"><span data-stu-id="db600-123">NOTES</span></span>

## <span data-ttu-id="db600-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db600-124">RELATED LINKS</span></span>
