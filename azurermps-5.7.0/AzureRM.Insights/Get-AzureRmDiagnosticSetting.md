---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
ms.openlocfilehash: b5963aa588672bb2a8940d3f61f4cd67bef9c4a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508135"
---
# <span data-ttu-id="0eed4-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="0eed4-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="0eed4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0eed4-102">SYNOPSIS</span></span>
<span data-ttu-id="0eed4-103">Ottiene le categorie registrate e i grani temporali.</span><span class="sxs-lookup"><span data-stu-id="0eed4-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0eed4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0eed4-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0eed4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0eed4-105">DESCRIPTION</span></span>
<span data-ttu-id="0eed4-106">Il cmdlet **Get-AzureRmDiagnosticSetting** ottiene le categorie e i grani temporali registrati per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="0eed4-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>

<span data-ttu-id="0eed4-107">Una granulosità temporale è l'intervallo di aggregazione di una metrica.</span><span class="sxs-lookup"><span data-stu-id="0eed4-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="0eed4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0eed4-108">EXAMPLES</span></span>

### <span data-ttu-id="0eed4-109">Esempio 1: ottenere lo stato delle categorie di registrazione e dei grani temporali</span><span class="sxs-lookup"><span data-stu-id="0eed4-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="0eed4-110">Questo comando ottiene le categorie e i grani temporali registrati per un Vault di chiave di Azure con un *resourceId* di/subscriptions/1a66ce04-B633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/Providers/Microsoft.keyvault/KeyVaults/ContosoKeyVault.</span><span class="sxs-lookup"><span data-stu-id="0eed4-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="0eed4-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0eed4-111">PARAMETERS</span></span>

### <span data-ttu-id="0eed4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eed4-112">-DefaultProfile</span></span>
<span data-ttu-id="0eed4-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0eed4-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0eed4-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0eed4-114">-ResourceId</span></span>
<span data-ttu-id="0eed4-115">Specifica l'ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0eed4-115">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="0eed4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eed4-116">CommonParameters</span></span>
<span data-ttu-id="0eed4-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eed4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eed4-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0eed4-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eed4-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0eed4-119">INPUTS</span></span>

### <span data-ttu-id="0eed4-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0eed4-120">None</span></span>
<span data-ttu-id="0eed4-121">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="0eed4-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0eed4-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0eed4-122">OUTPUTS</span></span>

### <span data-ttu-id="0eed4-123">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="0eed4-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="0eed4-124">Note</span><span class="sxs-lookup"><span data-stu-id="0eed4-124">NOTES</span></span>

## <span data-ttu-id="0eed4-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0eed4-125">RELATED LINKS</span></span>

[<span data-ttu-id="0eed4-126">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="0eed4-126">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


