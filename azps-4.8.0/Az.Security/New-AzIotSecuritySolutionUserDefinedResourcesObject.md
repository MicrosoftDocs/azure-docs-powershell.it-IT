---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionUserDefinedResourcesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
ms.openlocfilehash: e824c32ae2ae4f28972cdac9446eeeae6e410c75
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191939"
---
# <span data-ttu-id="7488e-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span><span class="sxs-lookup"><span data-stu-id="7488e-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span></span>

## <span data-ttu-id="7488e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7488e-102">SYNOPSIS</span></span>
<span data-ttu-id="7488e-103">Creare nuove risorse definite dall'utente per la soluzione di sicurezza degli utenti</span><span class="sxs-lookup"><span data-stu-id="7488e-103">Create new user defined resources for iot security solution</span></span>

## <span data-ttu-id="7488e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7488e-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionUserDefinedResourcesObject -Query <String> -QuerySubscriptionList <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7488e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7488e-105">DESCRIPTION</span></span>
<span data-ttu-id="7488e-106">Il cmdlet AzIotSecuritySolutionUserDefinedResourcesObject crea un nuovo oggetto Resources definito dall'utente per la soluzione di sicurezza per gli utenti.</span><span class="sxs-lookup"><span data-stu-id="7488e-106">The AzIotSecuritySolutionUserDefinedResourcesObject cmdlet creates a new user defined resources object for the iot security solution.</span></span>

## <span data-ttu-id="7488e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7488e-107">EXAMPLES</span></span>

### <span data-ttu-id="7488e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7488e-108">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")

Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
QuerySubscriptions: ["XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX"]
```

<span data-ttu-id="7488e-109">Creare nuove risorse definite dall'utente</span><span class="sxs-lookup"><span data-stu-id="7488e-109">Create new user defined resources</span></span>

## <span data-ttu-id="7488e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7488e-110">PARAMETERS</span></span>

### <span data-ttu-id="7488e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7488e-111">-DefaultProfile</span></span>
<span data-ttu-id="7488e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7488e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7488e-113">-Query</span><span class="sxs-lookup"><span data-stu-id="7488e-113">-Query</span></span>
<span data-ttu-id="7488e-114">Query.</span><span class="sxs-lookup"><span data-stu-id="7488e-114">Query.</span></span>

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

### <span data-ttu-id="7488e-115">-QuerySubscriptionList</span><span class="sxs-lookup"><span data-stu-id="7488e-115">-QuerySubscriptionList</span></span>
<span data-ttu-id="7488e-116">Sottoscrizioni di query.</span><span class="sxs-lookup"><span data-stu-id="7488e-116">Query subscriptions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7488e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7488e-117">CommonParameters</span></span>
<span data-ttu-id="7488e-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7488e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7488e-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7488e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7488e-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7488e-120">INPUTS</span></span>

### <span data-ttu-id="7488e-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7488e-121">None</span></span>

## <span data-ttu-id="7488e-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7488e-122">OUTPUTS</span></span>

### <span data-ttu-id="7488e-123">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="7488e-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

## <span data-ttu-id="7488e-124">Note</span><span class="sxs-lookup"><span data-stu-id="7488e-124">NOTES</span></span>

## <span data-ttu-id="7488e-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7488e-125">RELATED LINKS</span></span>
