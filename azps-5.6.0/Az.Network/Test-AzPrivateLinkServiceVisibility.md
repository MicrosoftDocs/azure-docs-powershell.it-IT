---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: 3fe05034734a4cfb0d511921372e41b00d7b457c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951710"
---
# <span data-ttu-id="625f2-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="625f2-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="625f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="625f2-102">SYNOPSIS</span></span>
<span data-ttu-id="625f2-103">**Test-AzPrivateLinkServiceVisibility** controlla se un servizio di collegamento privato è visibile per l'uso corrente.</span><span class="sxs-lookup"><span data-stu-id="625f2-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="625f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="625f2-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="625f2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="625f2-105">DESCRIPTION</span></span>
<span data-ttu-id="625f2-106">Verificare se un servizio di collegamento privato è visibile per l'uso corrente.</span><span class="sxs-lookup"><span data-stu-id="625f2-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="625f2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="625f2-107">EXAMPLES</span></span>

### <span data-ttu-id="625f2-108">Esempio 1: Verificare se contoso.cloudapp.azure.com è disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="625f2-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="625f2-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="625f2-109">PARAMETERS</span></span>

### <span data-ttu-id="625f2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="625f2-110">-DefaultProfile</span></span>
<span data-ttu-id="625f2-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="625f2-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="625f2-112">-Location</span><span class="sxs-lookup"><span data-stu-id="625f2-112">-Location</span></span>
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

### <span data-ttu-id="625f2-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="625f2-113">-PrivateLinkServiceAlias</span></span>
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

### <span data-ttu-id="625f2-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="625f2-114">-ResourceGroupName</span></span>
<span data-ttu-id="625f2-115">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="625f2-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="625f2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="625f2-116">CommonParameters</span></span>
<span data-ttu-id="625f2-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="625f2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="625f2-118">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="625f2-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="625f2-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="625f2-119">INPUTS</span></span>

### <span data-ttu-id="625f2-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="625f2-120">None</span></span>

## <span data-ttu-id="625f2-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="625f2-121">OUTPUTS</span></span>

### <span data-ttu-id="625f2-122">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="625f2-122">System.Boolean</span></span>

## <span data-ttu-id="625f2-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="625f2-123">NOTES</span></span>

## <span data-ttu-id="625f2-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="625f2-124">RELATED LINKS</span></span>
