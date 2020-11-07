---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermdiagnosticsetting
schema: 2.0.0
ms.openlocfilehash: eb7dbdee5d1d3d1574be30c5168d97dfcee6ab27
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865837"
---
# <span data-ttu-id="3d242-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="3d242-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="3d242-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3d242-102">SYNOPSIS</span></span>
<span data-ttu-id="3d242-103">Ottiene le categorie registrate e i grani temporali.</span><span class="sxs-lookup"><span data-stu-id="3d242-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d242-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d242-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d242-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d242-105">DESCRIPTION</span></span>
<span data-ttu-id="3d242-106">Il cmdlet **Get-AzureRmDiagnosticSetting** ottiene le categorie e i grani temporali registrati per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="3d242-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="3d242-107">Una granulosità temporale è l'intervallo di aggregazione di una metrica.</span><span class="sxs-lookup"><span data-stu-id="3d242-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="3d242-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d242-108">EXAMPLES</span></span>

### <span data-ttu-id="3d242-109">Esempio 1: ottenere lo stato delle categorie di registrazione e dei grani temporali</span><span class="sxs-lookup"><span data-stu-id="3d242-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="3d242-110">Questo comando ottiene le categorie e i grani temporali registrati per un Vault di chiave di Azure con un *resourceId* di/subscriptions/1a66ce04-B633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/Providers/Microsoft.keyvault/KeyVaults/ContosoKeyVault.</span><span class="sxs-lookup"><span data-stu-id="3d242-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="3d242-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3d242-111">PARAMETERS</span></span>

### <span data-ttu-id="3d242-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d242-112">-DefaultProfile</span></span>
<span data-ttu-id="3d242-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3d242-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d242-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d242-114">-Name</span></span>
<span data-ttu-id="3d242-115">Nome dell'impostazione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="3d242-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="3d242-116">Se non viene specificata la chiamata "Service" per impostazione predefinita, come nell'API precedente.</span><span class="sxs-lookup"><span data-stu-id="3d242-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="3d242-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d242-117">-ResourceId</span></span>
<span data-ttu-id="3d242-118">Specifica l'ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="3d242-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="3d242-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d242-119">CommonParameters</span></span>
<span data-ttu-id="3d242-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d242-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d242-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d242-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d242-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3d242-122">INPUTS</span></span>

### <span data-ttu-id="3d242-123">System. String</span><span class="sxs-lookup"><span data-stu-id="3d242-123">System.String</span></span>

## <span data-ttu-id="3d242-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d242-124">OUTPUTS</span></span>

### <span data-ttu-id="3d242-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="3d242-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="3d242-126">Note</span><span class="sxs-lookup"><span data-stu-id="3d242-126">NOTES</span></span>

## <span data-ttu-id="3d242-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d242-127">RELATED LINKS</span></span>

<span data-ttu-id="3d242-128">[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md) 
 [Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="3d242-128">[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)
[Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span></span>
