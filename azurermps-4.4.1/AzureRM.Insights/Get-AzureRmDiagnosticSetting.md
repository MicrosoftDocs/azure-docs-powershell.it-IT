---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 236ce405c222ba3b7746ba1affca8f288045f8a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687195"
---
# <span data-ttu-id="6fb69-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="6fb69-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="6fb69-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6fb69-102">SYNOPSIS</span></span>
<span data-ttu-id="6fb69-103">Ottiene le categorie registrate e i grani temporali.</span><span class="sxs-lookup"><span data-stu-id="6fb69-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fb69-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6fb69-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6fb69-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6fb69-105">DESCRIPTION</span></span>
<span data-ttu-id="6fb69-106">Il cmdlet **Get-AzureRmDiagnosticSetting** ottiene le categorie e i grani temporali registrati per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="6fb69-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>

<span data-ttu-id="6fb69-107">Una granulosità temporale è l'intervallo di aggregazione di una metrica.</span><span class="sxs-lookup"><span data-stu-id="6fb69-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="6fb69-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6fb69-108">EXAMPLES</span></span>

### <span data-ttu-id="6fb69-109">Esempio 1: ottenere lo stato delle categorie di registrazione e dei grani temporali</span><span class="sxs-lookup"><span data-stu-id="6fb69-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="6fb69-110">Questo comando ottiene le categorie e i grani temporali registrati per un Vault di chiave di Azure con un *resourceId* di/subscriptions/1a66ce04-B633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/Providers/Microsoft.keyvault/KeyVaults/ContosoKeyVault.</span><span class="sxs-lookup"><span data-stu-id="6fb69-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="6fb69-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6fb69-111">PARAMETERS</span></span>

### <span data-ttu-id="6fb69-112">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fb69-112">-ResourceId</span></span>
<span data-ttu-id="6fb69-113">Specifica l'ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6fb69-113">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="6fb69-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fb69-114">-DefaultProfile</span></span>
<span data-ttu-id="6fb69-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6fb69-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fb69-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fb69-116">CommonParameters</span></span>
<span data-ttu-id="6fb69-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fb69-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fb69-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fb69-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fb69-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6fb69-119">INPUTS</span></span>

## <span data-ttu-id="6fb69-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6fb69-120">OUTPUTS</span></span>

### <span data-ttu-id="6fb69-121">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="6fb69-121">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="6fb69-122">Note</span><span class="sxs-lookup"><span data-stu-id="6fb69-122">NOTES</span></span>

## <span data-ttu-id="6fb69-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6fb69-123">RELATED LINKS</span></span>

[<span data-ttu-id="6fb69-124">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="6fb69-124">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


