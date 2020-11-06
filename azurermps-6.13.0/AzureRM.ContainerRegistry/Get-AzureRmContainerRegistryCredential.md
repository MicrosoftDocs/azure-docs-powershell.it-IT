---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 37ca6fad019814c476f48d1f086a430db75afb99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507552"
---
# <span data-ttu-id="610f3-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="610f3-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="610f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="610f3-102">SYNOPSIS</span></span>
<span data-ttu-id="610f3-103">Ottiene le credenziali di accesso per un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="610f3-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="610f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="610f3-104">SYNTAX</span></span>

### <span data-ttu-id="610f3-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="610f3-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="610f3-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="610f3-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="610f3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="610f3-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="610f3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="610f3-108">DESCRIPTION</span></span>
<span data-ttu-id="610f3-109">Il cmdlet Get-AzureRmContainerRegistryCredential ottiene le credenziali di accesso per un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="610f3-109">The Get-AzureRmContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="610f3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="610f3-110">EXAMPLES</span></span>

### <span data-ttu-id="610f3-111">Esempio 1: ottenere le credenziali di accesso per un registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="610f3-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="610f3-112">Questo comando ottiene le credenziali di accesso per il registro di sistema contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="610f3-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="610f3-113">L'utente di amministratore deve essere abilitato per il registro \` di sistema Registry \` per ottenere le credenziali di accesso.</span><span class="sxs-lookup"><span data-stu-id="610f3-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="610f3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="610f3-114">PARAMETERS</span></span>

### <span data-ttu-id="610f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="610f3-115">-DefaultProfile</span></span>
<span data-ttu-id="610f3-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="610f3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="610f3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="610f3-117">-Name</span></span>
<span data-ttu-id="610f3-118">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="610f3-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="610f3-119">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="610f3-119">-Registry</span></span>
<span data-ttu-id="610f3-120">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="610f3-120">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610f3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="610f3-121">-ResourceGroupName</span></span>
<span data-ttu-id="610f3-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="610f3-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="610f3-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="610f3-123">-ResourceId</span></span>
<span data-ttu-id="610f3-124">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="610f3-124">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="610f3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="610f3-125">CommonParameters</span></span>
<span data-ttu-id="610f3-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="610f3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="610f3-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="610f3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="610f3-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="610f3-128">INPUTS</span></span>

### <span data-ttu-id="610f3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="610f3-129">System.String</span></span>

## <span data-ttu-id="610f3-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="610f3-130">OUTPUTS</span></span>

### <span data-ttu-id="610f3-131">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="610f3-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="610f3-132">Note</span><span class="sxs-lookup"><span data-stu-id="610f3-132">NOTES</span></span>

## <span data-ttu-id="610f3-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="610f3-133">RELATED LINKS</span></span>

[<span data-ttu-id="610f3-134">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="610f3-134">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="610f3-135">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="610f3-135">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="610f3-136">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="610f3-136">Update-AzureRmContainerRegistryCredential</span></span>](Update-AzureRmContainerRegistryCredential.md)

