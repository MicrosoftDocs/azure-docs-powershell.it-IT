---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappazurestoragepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
ms.openlocfilehash: 5571add1c12ac40279531274b47acfe67fc19734
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474761"
---
# <span data-ttu-id="b40a2-101">New-AzWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="b40a2-101">New-AzWebAppAzureStoragePath</span></span>

## <span data-ttu-id="b40a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b40a2-102">SYNOPSIS</span></span>
<span data-ttu-id="b40a2-103">Crea un oggetto che rappresenta un percorso di archiviazione di Azure da montare in un'app Web.</span><span class="sxs-lookup"><span data-stu-id="b40a2-103">Creates an object that represents an Azure Storage path to be mounted in a Web App.</span></span> <span data-ttu-id="b40a2-104">È concepito per essere usato come parametro (-AzureStoragePath) per Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b40a2-104">It is meant to be used as a parameter (-AzureStoragePath) to Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <span data-ttu-id="b40a2-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b40a2-105">SYNTAX</span></span>

```
New-AzWebAppAzureStoragePath -Name <String> -Type <AzureStorageType> -AccountName <String> -ShareName <String>
 -AccessKey <String> -MountPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b40a2-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b40a2-106">DESCRIPTION</span></span>
<span data-ttu-id="b40a2-107">Crea un oggetto che rappresenta un percorso di archiviazione di Azure da montare all'interno di un'app Web.</span><span class="sxs-lookup"><span data-stu-id="b40a2-107">Creates an object that represent an Azure Storage path to be mounted inside a Web App.</span></span>

## <span data-ttu-id="b40a2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b40a2-108">EXAMPLES</span></span>

### <span data-ttu-id="b40a2-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b40a2-109">Example 1</span></span>
```powershell
PS C:\> $storagePath1 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount1" -AccountName "myaccount.files.core.windows.net" -Type AzureFiles -ShareName "someShareName" -AccessKey "some access key"
-MountPath "C:\myFolderInsideTheContainerWebApp" 

PS C:\> $storagePath2 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount2" -AccountName "myaccount2.files.core.windows.net" -Type AzureFiles -ShareName "someShareName2" -AccessKey "some access key 2"
-MountPath "C:\myFolderInsideTheContainerWebApp2" 

PS C:\> Set-AzWebApp -ResourceGroup myresourcegroup -Name myapp -AzureStoragePath $storagepath1, $storagePath2
```

## <span data-ttu-id="b40a2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b40a2-110">PARAMETERS</span></span>

### <span data-ttu-id="b40a2-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="b40a2-111">-AccessKey</span></span>
<span data-ttu-id="b40a2-112">Chiave di accesso all'account di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="b40a2-112">Access key to the Azure Storage account</span></span>

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

### <span data-ttu-id="b40a2-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b40a2-113">-AccountName</span></span>
<span data-ttu-id="b40a2-114">Nome dell'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b40a2-114">Azure Storage account name.</span></span>
<span data-ttu-id="b40a2-115">Ad esempio: myfilestorageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="b40a2-115">E.g.: myfilestorageaccount.file.core.windows.net</span></span>

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

### <span data-ttu-id="b40a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b40a2-116">-DefaultProfile</span></span>
<span data-ttu-id="b40a2-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b40a2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b40a2-118">-MountPath</span><span class="sxs-lookup"><span data-stu-id="b40a2-118">-MountPath</span></span>
<span data-ttu-id="b40a2-119">Percorso nel contenitore in cui verrà esposta la condivisione specificata da ShareName</span><span class="sxs-lookup"><span data-stu-id="b40a2-119">Path in the container where the share specified by ShareName will be exposed</span></span>

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

### <span data-ttu-id="b40a2-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b40a2-120">-Name</span></span>
<span data-ttu-id="b40a2-121">Identificatore della proprietà di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b40a2-121">The identifier of the Azure Storage property.</span></span>
<span data-ttu-id="b40a2-122">Deve essere univoco all'interno dell'app Web o dello slot</span><span class="sxs-lookup"><span data-stu-id="b40a2-122">Must be unique within the Web App or Slot</span></span>

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

### <span data-ttu-id="b40a2-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b40a2-123">-ShareName</span></span>
<span data-ttu-id="b40a2-124">Nome della condivisione da montare nel contenitore</span><span class="sxs-lookup"><span data-stu-id="b40a2-124">Name of the share to mount to the container</span></span>

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

### <span data-ttu-id="b40a2-125">-Digitare</span><span class="sxs-lookup"><span data-stu-id="b40a2-125">-Type</span></span>
<span data-ttu-id="b40a2-126">Tipo di account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b40a2-126">Type of Azure Storage account.</span></span>
<span data-ttu-id="b40a2-127">I contenitori Windows supportano solo i file Azure</span><span class="sxs-lookup"><span data-stu-id="b40a2-127">Windows Containers only supports Azure Files</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.AzureStorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureFiles, AzureBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b40a2-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b40a2-128">-Confirm</span></span>
<span data-ttu-id="b40a2-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b40a2-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b40a2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b40a2-130">-WhatIf</span></span>
<span data-ttu-id="b40a2-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b40a2-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b40a2-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b40a2-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b40a2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b40a2-133">CommonParameters</span></span>
<span data-ttu-id="b40a2-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b40a2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b40a2-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b40a2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b40a2-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b40a2-136">INPUTS</span></span>

### <span data-ttu-id="b40a2-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b40a2-137">None</span></span>

## <span data-ttu-id="b40a2-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b40a2-138">OUTPUTS</span></span>

### <span data-ttu-id="b40a2-139">Microsoft. Azure. Commands. webapps. Models. WebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="b40a2-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span></span>

## <span data-ttu-id="b40a2-140">Note</span><span class="sxs-lookup"><span data-stu-id="b40a2-140">NOTES</span></span>

## <span data-ttu-id="b40a2-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b40a2-141">RELATED LINKS</span></span>
