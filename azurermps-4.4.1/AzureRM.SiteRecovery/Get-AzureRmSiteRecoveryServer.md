---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: CFB7CF64-1415-44B3-932B-2A5613666D3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: aacb061772ed1b1202528ebc7b7bc95d725bb9f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687682"
---
# <span data-ttu-id="06944-101">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="06944-101">Get-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="06944-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06944-102">SYNOPSIS</span></span>
<span data-ttu-id="06944-103">Ottiene informazioni sui server di ripristino del sito registrati nel Vault corrente.</span><span class="sxs-lookup"><span data-stu-id="06944-103">Gets information about Site Recovery servers registered to the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06944-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06944-104">SYNTAX</span></span>

### <span data-ttu-id="06944-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="06944-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06944-106">ByName</span><span class="sxs-lookup"><span data-stu-id="06944-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServer -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06944-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="06944-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06944-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06944-108">DESCRIPTION</span></span>
<span data-ttu-id="06944-109">Il cmdlet **Get-AzureRmSiteRecoveryServer** ottiene informazioni sui server di ripristino dei siti di Azure registrati nell'attuale archivio di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="06944-109">The **Get-AzureRmSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="06944-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06944-110">EXAMPLES</span></span>

## <span data-ttu-id="06944-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06944-111">PARAMETERS</span></span>

### <span data-ttu-id="06944-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="06944-112">-FriendlyName</span></span>
<span data-ttu-id="06944-113">Specifica il nome descrittivo del server.</span><span class="sxs-lookup"><span data-stu-id="06944-113">Specifies the friendly name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06944-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="06944-114">-Name</span></span>
<span data-ttu-id="06944-115">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="06944-115">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06944-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06944-116">-DefaultProfile</span></span>
<span data-ttu-id="06944-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06944-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06944-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06944-118">CommonParameters</span></span>
<span data-ttu-id="06944-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06944-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06944-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06944-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06944-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06944-121">INPUTS</span></span>

## <span data-ttu-id="06944-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06944-122">OUTPUTS</span></span>

### <span data-ttu-id="06944-123">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="06944-123">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="06944-124">Note</span><span class="sxs-lookup"><span data-stu-id="06944-124">NOTES</span></span>

## <span data-ttu-id="06944-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06944-125">RELATED LINKS</span></span>

[<span data-ttu-id="06944-126">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="06944-126">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
