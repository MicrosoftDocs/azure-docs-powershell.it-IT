---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: f3fb2377fd78db4b330afd39a8691f958597f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511196"
---
# <span data-ttu-id="c5173-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="c5173-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="c5173-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5173-102">SYNOPSIS</span></span>

<span data-ttu-id="c5173-103">Sincronizza un database specificato nell'istanza specificata di Analysis Services server in tutte le istanze di scalabilità delle query nell'ambiente attualmente connesso, come specificato in comando Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c5173-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5173-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5173-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-Passthru]
```

## <span data-ttu-id="c5173-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5173-105">DESCRIPTION</span></span>

<span data-ttu-id="c5173-106">Il cmdlet Sync-AzureAnalysisServicesInstance sincronizza un database specificato nell'istanza specificata di Analysis Services server per tutte le istanze di scalabilità delle query nell'ambiente attualmente connesso, come specificato in Add-AzureAnalysisServicesAccount comando</span><span class="sxs-lookup"><span data-stu-id="c5173-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="c5173-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5173-107">EXAMPLES</span></span>

### <span data-ttu-id="c5173-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c5173-108">Example 1</span></span>

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="c5173-109">Questo comando Sincronizza il database denominato SalesOrders nel server denominato ' Contoso ' nell'ambiente westus.asazure.windows.net a condizione che l'utente abbia effettuato l'accesso a questo ambiente usando il comando Add-AzureAnalysisServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="c5173-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="c5173-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5173-110">PARAMETERS</span></span>

### <span data-ttu-id="c5173-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="c5173-111">-Instance</span></span>

<span data-ttu-id="c5173-112">Nome dell'istanza del server Analysis Services da riavviare</span><span class="sxs-lookup"><span data-stu-id="c5173-112">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5173-113">-Database</span><span class="sxs-lookup"><span data-stu-id="c5173-113">-Database</span></span>

<span data-ttu-id="c5173-114">Identità del database da sincronizzare</span><span class="sxs-lookup"><span data-stu-id="c5173-114">Identity of the database to be synchronized</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5173-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5173-115">-PassThru</span></span>

<span data-ttu-id="c5173-116">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="c5173-116">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: Switch
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="c5173-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5173-117">INPUTS</span></span>

### <span data-ttu-id="c5173-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c5173-118">None</span></span>
<span data-ttu-id="c5173-119">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c5173-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c5173-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5173-120">OUTPUTS</span></span>

### <span data-ttu-id="c5173-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c5173-121">System.Boolean</span></span>

## <span data-ttu-id="c5173-122">Note</span><span class="sxs-lookup"><span data-stu-id="c5173-122">NOTES</span></span>

<span data-ttu-id="c5173-123">Alias: Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="c5173-123">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="c5173-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5173-124">RELATED LINKS</span></span>
