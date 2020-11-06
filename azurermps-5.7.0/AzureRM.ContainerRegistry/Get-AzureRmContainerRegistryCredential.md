---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 68ef1cf00adeec785faf3c3f43ff2e7dbcaafbc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521065"
---
# <span data-ttu-id="fe78c-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="fe78c-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="fe78c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe78c-102">SYNOPSIS</span></span>
<span data-ttu-id="fe78c-103">Ottiene le credenziali di accesso per un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="fe78c-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe78c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe78c-104">SYNTAX</span></span>

### <span data-ttu-id="fe78c-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fe78c-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe78c-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe78c-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe78c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe78c-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe78c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe78c-108">DESCRIPTION</span></span>
<span data-ttu-id="fe78c-109">Il cmdlet Get-AzureRmContainerRegistryCredential ottiene le credenziali di accesso per un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="fe78c-109">The Get-AzureRmContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="fe78c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe78c-110">EXAMPLES</span></span>

### <span data-ttu-id="fe78c-111">Esempio 1: ottenere le credenziali di accesso per un registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="fe78c-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="fe78c-112">Questo comando ottiene le credenziali di accesso per il registro di sistema contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="fe78c-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="fe78c-113">L'utente di amministratore deve essere abilitato per il registro \` di sistema Registry \` per ottenere le credenziali di accesso.</span><span class="sxs-lookup"><span data-stu-id="fe78c-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="fe78c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe78c-114">PARAMETERS</span></span>

### <span data-ttu-id="fe78c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe78c-115">-Name</span></span>
<span data-ttu-id="fe78c-116">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="fe78c-116">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe78c-117">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="fe78c-117">-Registry</span></span>
<span data-ttu-id="fe78c-118">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="fe78c-118">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe78c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe78c-119">-ResourceGroupName</span></span>
<span data-ttu-id="fe78c-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fe78c-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe78c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe78c-121">-DefaultProfile</span></span>
<span data-ttu-id="fe78c-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fe78c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe78c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe78c-123">-ResourceId</span></span>
<span data-ttu-id="fe78c-124">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="fe78c-124">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe78c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe78c-125">CommonParameters</span></span>
<span data-ttu-id="fe78c-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe78c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe78c-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe78c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe78c-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe78c-128">INPUTS</span></span>

### <span data-ttu-id="fe78c-129">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fe78c-129">PSContainerRegistry</span></span>
<span data-ttu-id="fe78c-130">Il parametro ' Registry ' accetta il valore di tipo ' PSContainerRegistry ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="fe78c-130">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="fe78c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe78c-131">OUTPUTS</span></span>

### <span data-ttu-id="fe78c-132">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="fe78c-132">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="fe78c-133">Note</span><span class="sxs-lookup"><span data-stu-id="fe78c-133">NOTES</span></span>

## <span data-ttu-id="fe78c-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe78c-134">RELATED LINKS</span></span>

[<span data-ttu-id="fe78c-135">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fe78c-135">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="fe78c-136">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fe78c-136">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="fe78c-137">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="fe78c-137">Update-AzureRmContainerRegistryCredential</span></span>](Update-AzureRmContainerRegistryCredential.md)

