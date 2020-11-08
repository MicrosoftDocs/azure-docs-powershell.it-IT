---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: a4a365cdaee79a39b87331c42c832e40f7cbd657
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191491"
---
# <span data-ttu-id="546df-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="546df-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="546df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="546df-102">SYNOPSIS</span></span>
<span data-ttu-id="546df-103">Ottiene un elenco delle definizioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="546df-103">Gets a list of the registration definitions.</span></span>

## <span data-ttu-id="546df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="546df-104">SYNTAX</span></span>

### <span data-ttu-id="546df-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="546df-105">Default (Default)</span></span>
```
Get-AzManagedServicesDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="546df-106">ById</span><span class="sxs-lookup"><span data-stu-id="546df-106">ById</span></span>
```
Get-AzManagedServicesDefinition -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="546df-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="546df-107">ByResourceId</span></span>
```
Get-AzManagedServicesDefinition -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="546df-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="546df-108">DESCRIPTION</span></span>
<span data-ttu-id="546df-109">Ottiene un elenco delle definizioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="546df-109">Gets a list of the registration definitions.</span></span>

## <span data-ttu-id="546df-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="546df-110">EXAMPLES</span></span>

### <span data-ttu-id="546df-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="546df-111">Example 1</span></span>
```powershell
PS C:\> Get-AzManagedServicesDefinition

Name                                 ManagedByTenantId                    PrincipalId                                                                  RoleDefinitionId
----                                 -----------------                    -----------                                                                  ----------------
fff287a4-1714-4a17-bc40-a17ca8e69e3f bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671                                         acdd72a7-3385-48ef-bd42-f606fba81ae7
ee7e40e8-bc3f-4624-b0ca-d5364635b141 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671                                         acdd72a7-3385-48ef-bd42-f606fba81ae7
e2ddcd3c-d50f-4d51-afd9-f9132fcae4e7 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671                                         acdd72a7-3385-48ef-bd42-f606fba81ae7
d3301f65-7087-438c-a6bc-4b7ead094889 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671                                         acdd72a7-3385-48ef-bd42-f606fba81ae7
cae481c0-de7c-42a8-86c1-5b170861caf8 bab3375b-6197-4a15-a44b-16c41faa91d7 {d6f6c88a-5b7a-455e-ba40-ce146d4d3671, d6f6c88a-5b7a-455e-ba40-ce146d4d3671} {acdd72a7-3385-48ef-bd42-f606fba81ae7, b24988ac-6180-42a0-ab88-20f7382dd24c}
bb2626be-3e11-442f-b0f1-9209508d4f52 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671                                         acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="546df-112">Ottiene tutte le definizioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="546df-112">Gets all registration definitions.</span></span>

### <span data-ttu-id="546df-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="546df-113">Example 2</span></span>
```powershell
PS C:\> Get-AzManagedServicesDefinition -Id fff287a4-1714-4a17-bc40-a17ca8e69e3f

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
fff287a4-1714-4a17-bc40-a17ca8e69e3f bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="546df-114">Ottiene la definizione di registrazione in base all'ID.</span><span class="sxs-lookup"><span data-stu-id="546df-114">Gets the registration definition given its id.</span></span>

### <span data-ttu-id="546df-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="546df-115">Example 3</span></span>
```powershell
PS C:\> $definitions = Get-AzManagedServicesDefinition
PS C:\> $definitions[0].Id
/subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/fff287a4-1714-4a17-bc40-a17ca8e69e3f
PS C:\> Get-AzManagedServicesDefinition -ResourceId $definitions[0].Id

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
fff287a4-1714-4a17-bc40-a17ca8e69e3f bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="546df-116">Ottiene la definizione di registrazione in base all'ID risorsa completo.</span><span class="sxs-lookup"><span data-stu-id="546df-116">Gets the registration definition given the fully qualified resource id.</span></span>

## <span data-ttu-id="546df-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="546df-117">PARAMETERS</span></span>

### <span data-ttu-id="546df-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="546df-118">-DefaultProfile</span></span>
<span data-ttu-id="546df-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="546df-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="546df-120">-ID</span><span class="sxs-lookup"><span data-stu-id="546df-120">-Id</span></span>
<span data-ttu-id="546df-121">Identificatore della definizione di registrazione (ad esempio, b0c052e5-c437-4771-A476-8b1201158a57).</span><span class="sxs-lookup"><span data-stu-id="546df-121">The registration definition identifier (for example, b0c052e5-c437-4771-a476-8b1201158a57).</span></span>
```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="546df-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="546df-122">-ResourceId</span></span>
<span data-ttu-id="546df-123">ID risorsa completo della definizione di registrazione (ad esempio,/subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationDefinitions/b0c052e5-c437-4771-a476-8b1201158a57)</span><span class="sxs-lookup"><span data-stu-id="546df-123">The fully qualified resource id of the registration definition (for example, /subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationDefinitions/b0c052e5-c437-4771-a476-8b1201158a57)</span></span>
```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="546df-124">CommonParameters</span></span>
<span data-ttu-id="546df-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="546df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="546df-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="546df-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="546df-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="546df-127">INPUTS</span></span>

### <span data-ttu-id="546df-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="546df-128">None</span></span>

## <span data-ttu-id="546df-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="546df-129">OUTPUTS</span></span>

### <span data-ttu-id="546df-130">Microsoft. Azure. PowerShell. Cmdlets. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="546df-130">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="546df-131">Note</span><span class="sxs-lookup"><span data-stu-id="546df-131">NOTES</span></span>

## <span data-ttu-id="546df-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="546df-132">RELATED LINKS</span></span>
