---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: 5282b3d0ae145088cf07040520050937f8d3a335
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476852"
---
# <span data-ttu-id="6eda9-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="6eda9-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="6eda9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6eda9-102">SYNOPSIS</span></span>
<span data-ttu-id="6eda9-103">Ottiene una definizione di registrazione specifica o un elenco delle definizioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="6eda9-103">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="6eda9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6eda9-104">SYNTAX</span></span>

### <span data-ttu-id="6eda9-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6eda9-105">ByName (Default)</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6eda9-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="6eda9-106">Default</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6eda9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6eda9-107">DESCRIPTION</span></span>
<span data-ttu-id="6eda9-108">Ottiene una definizione di registrazione specifica o un elenco delle definizioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="6eda9-108">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="6eda9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6eda9-109">EXAMPLES</span></span>

### <span data-ttu-id="6eda9-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6eda9-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesDefinition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="6eda9-111">Ottiene tutte le definizioni di registrazione in ambito predefinito.</span><span class="sxs-lookup"><span data-stu-id="6eda9-111">Gets all registration definitions at default scope.</span></span>

### <span data-ttu-id="6eda9-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6eda9-112">Example 2</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="6eda9-113">Ottiene la definizione di registrazione per nome nell'ambito predefinito.</span><span class="sxs-lookup"><span data-stu-id="6eda9-113">Gets the registration definition by name at default scope.</span></span>

### <span data-ttu-id="6eda9-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6eda9-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="6eda9-115">Ottiene tutte le definizioni di registrazione nell'ambito indicato.</span><span class="sxs-lookup"><span data-stu-id="6eda9-115">Gets all registration definitions at the given scope.</span></span>

## <span data-ttu-id="6eda9-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6eda9-116">PARAMETERS</span></span>

### <span data-ttu-id="6eda9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eda9-117">-DefaultProfile</span></span>
<span data-ttu-id="6eda9-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6eda9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6eda9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6eda9-119">-Name</span></span>
<span data-ttu-id="6eda9-120">Nome univoco della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="6eda9-120">The unique name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eda9-121">-Ambito</span><span class="sxs-lookup"><span data-stu-id="6eda9-121">-Scope</span></span>
<span data-ttu-id="6eda9-122">Ambito in cui è stata creata la definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="6eda9-122">The scope where the registration definition created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eda9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eda9-123">CommonParameters</span></span>
<span data-ttu-id="6eda9-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eda9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eda9-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6eda9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eda9-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6eda9-126">INPUTS</span></span>

### <span data-ttu-id="6eda9-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6eda9-127">None</span></span>
## <span data-ttu-id="6eda9-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6eda9-128">OUTPUTS</span></span>

### <span data-ttu-id="6eda9-129">Microsoft. Azure. PowerShell. Cmdlets. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="6eda9-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="6eda9-130">Note</span><span class="sxs-lookup"><span data-stu-id="6eda9-130">NOTES</span></span>

## <span data-ttu-id="6eda9-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6eda9-131">RELATED LINKS</span></span>
