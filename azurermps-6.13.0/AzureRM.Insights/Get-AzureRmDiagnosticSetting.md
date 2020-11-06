---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 2b70fd58bd0b51e03079b1c24665b67ac3ad3a2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515259"
---
# <span data-ttu-id="ff0be-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="ff0be-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="ff0be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff0be-102">SYNOPSIS</span></span>
<span data-ttu-id="ff0be-103">Ottiene le categorie registrate e i grani temporali.</span><span class="sxs-lookup"><span data-stu-id="ff0be-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff0be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff0be-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff0be-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff0be-105">DESCRIPTION</span></span>
<span data-ttu-id="ff0be-106">Il cmdlet **Get-AzureRmDiagnosticSetting** ottiene le categorie e i grani temporali registrati per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="ff0be-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="ff0be-107">Una granulosità temporale è l'intervallo di aggregazione di una metrica.</span><span class="sxs-lookup"><span data-stu-id="ff0be-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="ff0be-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff0be-108">EXAMPLES</span></span>

### <span data-ttu-id="ff0be-109">Esempio 1: ottenere lo stato delle categorie di registrazione e dei grani temporali</span><span class="sxs-lookup"><span data-stu-id="ff0be-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="ff0be-110">Questo comando ottiene le categorie e i grani temporali registrati per un Vault di chiave di Azure con un *resourceId* di/subscriptions/1a66ce04-B633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/Providers/Microsoft.keyvault/KeyVaults/ContosoKeyVault.</span><span class="sxs-lookup"><span data-stu-id="ff0be-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="ff0be-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff0be-111">PARAMETERS</span></span>

### <span data-ttu-id="ff0be-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff0be-112">-DefaultProfile</span></span>
<span data-ttu-id="ff0be-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ff0be-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff0be-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff0be-114">-Name</span></span>
<span data-ttu-id="ff0be-115">Nome dell'impostazione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="ff0be-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="ff0be-116">Se non viene specificata la chiamata "Service" per impostazione predefinita, come nell'API precedente.</span><span class="sxs-lookup"><span data-stu-id="ff0be-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="ff0be-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff0be-117">-ResourceId</span></span>
<span data-ttu-id="ff0be-118">Specifica l'ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ff0be-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="ff0be-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff0be-119">CommonParameters</span></span>
<span data-ttu-id="ff0be-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff0be-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff0be-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff0be-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff0be-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff0be-122">INPUTS</span></span>

### <span data-ttu-id="ff0be-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ff0be-123">System.String</span></span>

## <span data-ttu-id="ff0be-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff0be-124">OUTPUTS</span></span>

### <span data-ttu-id="ff0be-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="ff0be-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="ff0be-126">Note</span><span class="sxs-lookup"><span data-stu-id="ff0be-126">NOTES</span></span>

## <span data-ttu-id="ff0be-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff0be-127">RELATED LINKS</span></span>

<span data-ttu-id="ff0be-128">[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md) 
 [Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="ff0be-128">[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)
[Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span></span>
