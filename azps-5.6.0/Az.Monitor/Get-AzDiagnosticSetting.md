---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
ms.openlocfilehash: 9cfe797482485abccdce8e7094b3f5caadf554ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980062"
---
# <span data-ttu-id="8cac1-101">Get-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="8cac1-101">Get-AzDiagnosticSetting</span></span>

## <span data-ttu-id="8cac1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cac1-102">SYNOPSIS</span></span>
<span data-ttu-id="8cac1-103">Recupera le categorie e i grani tempo registrati.</span><span class="sxs-lookup"><span data-stu-id="8cac1-103">Gets the logged categories and time grains.</span></span>

## <span data-ttu-id="8cac1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cac1-104">SYNTAX</span></span>

```
Get-AzDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8cac1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8cac1-105">DESCRIPTION</span></span>
<span data-ttu-id="8cac1-106">Il cmdlet **Get-AzDiagnosticSetting** ottiene le categorie e i grana tempo registrati per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="8cac1-106">The **Get-AzDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="8cac1-107">Una granularità temporale è l'intervallo di aggregazione di una metrica.</span><span class="sxs-lookup"><span data-stu-id="8cac1-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="8cac1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cac1-108">EXAMPLES</span></span>

### <span data-ttu-id="8cac1-109">Esempio 1: Ottenere lo stato delle categorie di registrazione e dei grani tempo</span><span class="sxs-lookup"><span data-stu-id="8cac1-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="8cac1-110">Questo comando recupera le categorie e i granulari tempori registrati per un Vault delle chiavi di Azure con *resourceId* di /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span><span class="sxs-lookup"><span data-stu-id="8cac1-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="8cac1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8cac1-111">PARAMETERS</span></span>

### <span data-ttu-id="8cac1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cac1-112">-DefaultProfile</span></span>
<span data-ttu-id="8cac1-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8cac1-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cac1-114">-Name</span><span class="sxs-lookup"><span data-stu-id="8cac1-114">-Name</span></span>
<span data-ttu-id="8cac1-115">Nome dell'impostazione diagnostica.</span><span class="sxs-lookup"><span data-stu-id="8cac1-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="8cac1-116">Se la chiamata non viene specificata per impostazione predefinita su "servizio", come nell'API precedente.</span><span class="sxs-lookup"><span data-stu-id="8cac1-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="8cac1-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cac1-117">-ResourceId</span></span>
<span data-ttu-id="8cac1-118">Specifica l'ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8cac1-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="8cac1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cac1-119">CommonParameters</span></span>
<span data-ttu-id="8cac1-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cac1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cac1-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8cac1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cac1-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="8cac1-122">INPUTS</span></span>

### <span data-ttu-id="8cac1-123">System.String</span><span class="sxs-lookup"><span data-stu-id="8cac1-123">System.String</span></span>

## <span data-ttu-id="8cac1-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cac1-124">OUTPUTS</span></span>

### <span data-ttu-id="8cac1-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="8cac1-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="8cac1-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="8cac1-126">NOTES</span></span>

## <span data-ttu-id="8cac1-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cac1-127">RELATED LINKS</span></span>

<span data-ttu-id="8cac1-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="8cac1-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
