---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: fc9d8db7f293ff94e33b50afd55176d157046fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518319"
---
# <span data-ttu-id="aae84-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="aae84-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="aae84-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aae84-102">SYNOPSIS</span></span>
<span data-ttu-id="aae84-103">Ottiene le credenziali di accesso per un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="aae84-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aae84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aae84-104">SYNTAX</span></span>

### <span data-ttu-id="aae84-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aae84-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aae84-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aae84-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aae84-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aae84-107">DESCRIPTION</span></span>
<span data-ttu-id="aae84-108">Il cmdlet **Get-AzureRmContainerRegistryCredential** ottiene le credenziali di accesso per un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="aae84-108">The **Get-AzureRmContainerRegistryCredential** cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="aae84-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aae84-109">EXAMPLES</span></span>

### <span data-ttu-id="aae84-110">Esempio 1: ottenere le credenziali di accesso per un registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="aae84-110">Example 1: Get the login credentials for a container registry</span></span>
```
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="aae84-111">Questo comando ottiene le credenziali di accesso per il registro di sistema contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="aae84-111">This command gets the login credentials for the specified container registry.</span></span> <span data-ttu-id="aae84-112">L'utente amministratore deve essere abilitato per il registro di sistema del contenitore `MyRegistry` per ottenere le credenziali di accesso.</span><span class="sxs-lookup"><span data-stu-id="aae84-112">Admin user has to be enabled for the container registry `MyRegistry` to get login credentials.</span></span>

## <span data-ttu-id="aae84-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aae84-113">PARAMETERS</span></span>

### <span data-ttu-id="aae84-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="aae84-114">-Name</span></span>
<span data-ttu-id="aae84-115">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="aae84-115">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aae84-116">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="aae84-116">-Registry</span></span>
<span data-ttu-id="aae84-117">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="aae84-117">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aae84-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aae84-118">-ResourceGroupName</span></span>
<span data-ttu-id="aae84-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aae84-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aae84-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aae84-120">-DefaultProfile</span></span>
<span data-ttu-id="aae84-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aae84-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aae84-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aae84-122">CommonParameters</span></span>
<span data-ttu-id="aae84-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aae84-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aae84-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aae84-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aae84-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aae84-125">INPUTS</span></span>

### <span data-ttu-id="aae84-126">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="aae84-126">PSContainerRegistry</span></span>
<span data-ttu-id="aae84-127">Il parametro ' Registry ' accetta il valore di tipo ' PSContainerRegistry ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="aae84-127">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="aae84-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aae84-128">OUTPUTS</span></span>

### <span data-ttu-id="aae84-129">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="aae84-129">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="aae84-130">Note</span><span class="sxs-lookup"><span data-stu-id="aae84-130">NOTES</span></span>

## <span data-ttu-id="aae84-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aae84-131">RELATED LINKS</span></span>

[<span data-ttu-id="aae84-132">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="aae84-132">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="aae84-133">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="aae84-133">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="aae84-134">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="aae84-134">Update-AzureRmContainerRegistryCredential</span></span>](./Update-AzureRmContainerRegistryCredential.md)

