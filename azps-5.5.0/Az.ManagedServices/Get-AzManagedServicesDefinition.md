---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: 5282b3d0ae145088cf07040520050937f8d3a335
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187479"
---
# <span data-ttu-id="add12-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="add12-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="add12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="add12-102">SYNOPSIS</span></span>
<span data-ttu-id="add12-103">Ottiene una definizione di registrazione specifica o un elenco delle definizioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="add12-103">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="add12-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="add12-104">SYNTAX</span></span>

### <span data-ttu-id="add12-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="add12-105">ByName (Default)</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="add12-106">Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="add12-106">Default</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="add12-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="add12-107">DESCRIPTION</span></span>
<span data-ttu-id="add12-108">Ottiene una definizione di registrazione specifica o un elenco delle definizioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="add12-108">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="add12-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="add12-109">EXAMPLES</span></span>

### <span data-ttu-id="add12-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="add12-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesDefinition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="add12-111">Recupera tutte le definizioni di registrazione nell'ambito predefinito.</span><span class="sxs-lookup"><span data-stu-id="add12-111">Gets all registration definitions at default scope.</span></span>

### <span data-ttu-id="add12-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="add12-112">Example 2</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="add12-113">Ottiene la definizione di registrazione per nome nell'ambito predefinito.</span><span class="sxs-lookup"><span data-stu-id="add12-113">Gets the registration definition by name at default scope.</span></span>

### <span data-ttu-id="add12-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="add12-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="add12-115">Ottiene tutte le definizioni di registrazione nell'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="add12-115">Gets all registration definitions at the given scope.</span></span>

## <span data-ttu-id="add12-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="add12-116">PARAMETERS</span></span>

### <span data-ttu-id="add12-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="add12-117">-DefaultProfile</span></span>
<span data-ttu-id="add12-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="add12-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="add12-119">-Name</span><span class="sxs-lookup"><span data-stu-id="add12-119">-Name</span></span>
<span data-ttu-id="add12-120">Nome univoco della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="add12-120">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="add12-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="add12-121">-Scope</span></span>
<span data-ttu-id="add12-122">Ambito in cui è stata creata la definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="add12-122">The scope where the registration definition created.</span></span>

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

### <span data-ttu-id="add12-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add12-123">CommonParameters</span></span>
<span data-ttu-id="add12-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="add12-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add12-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="add12-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add12-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="add12-126">INPUTS</span></span>

### <span data-ttu-id="add12-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="add12-127">None</span></span>
## <span data-ttu-id="add12-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="add12-128">OUTPUTS</span></span>

### <span data-ttu-id="add12-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="add12-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="add12-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="add12-130">NOTES</span></span>

## <span data-ttu-id="add12-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="add12-131">RELATED LINKS</span></span>
